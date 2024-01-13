---
{"wordcount":0,"dg-publish":true,"permalink":"/coding/website-building/panic-button/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-11-14T21:08:37.123+05:30","updated":"2024-01-13T18:48:17.679+05:30"}
---

🧶 Tags:: #Code 
==2023-06-11 - 10:33==

I saw a Chrome extension that hides your tabs and opens a different one with a simple panic button. This can be useful in different scenarios, like if you're seeing something NSFW and need to hide it quickly.

<img src="https://exiasgarden.pages.dev/wp-content/uploads/2023/06/Panic-button-1024x576.webp">

So I decided I should build one myself. Mind you I've never made an extension before so had to do some digging and also had to take some help from chatGPT as I some of the JavaScript to reopen tabs was a bit tricky for my level.

After some tinkering it is now finished.

## How to Use It?
If you're using normal chrome browser you can just go to the extensions tab and drag and drop the .crx file to install it. Although for me that's not possible as I'm using brave, but for the good part I can turn on the developer option and install the unpacked(folder with individual files) extension easily, and you can do it too, if you want.

You can download the code folder from here - [MEGA](https://mega.nz/folder/QMFnDTLT#myiZp-fL2OsbyOB5pEb_Zg). The code is available below and also on [github](https://github.com/ooexiaoo/Panic-Button-Extension) if you want to copy or take a look at it.
### Go to Extensions Tab
![extension options tab.webp](/img/user/extension%20options%20tab.webp)

### Turn On Developer Mode
![turning on developer mode.webp](/img/user/turning%20on%20developer%20mode.webp)

### Click Load Unpacked Option
![load unpacked.webp](/img/user/load%20unpacked.webp)

### Select the Extension Folder You Want to Use
![v.1.webp](/img/user/v.1.webp)
Here I have V.1 because I made a few version, You will have just one folder.

![Click options tab.webp](/img/user/Click%20options%20tab.webp)

After installing the extension you'd have to click on **"options"** tab. This will open an options tab in which you can add the safe website address you want. Remember to add **"https://"** before the website name otherwise it'll show an error. **I.e add - "https://example.com" instead of "example.com".**

After adding the website name it will show a confirmation message saying the **" Safe website URL saved"**. With that you're good to go!

![panic button options.webp](/img/user/panic%20button%20options.webp)

Now you can use **"Ctrl+Shift+K"** to open a safe website and minimize the chrome window you were on. Pressing the same keys again will close the safe website and maximize the original window that was open.

## Here's the Code
### Manifest.json
```json
{
  "manifest_version": 2,
  "name": "Panic Button Extension",
  "version": "1.0",
  "description": "By pressing Ctrl+Shift+K you can switch to a safe window quickly. Go in extension options to add your safe window.",
  "permissions": ["tabs", "storage"],
  "background": {
    "scripts": ["background.js"],
    "persistent": false
  },
  "options_ui": {
    "page": "options.html",
    "open_in_tab": true
  },
  "icons": {
    "16": "icon.png",
    "48": "icon.png",
    "128": "icon.png"
  },
  "commands": {
    "toggle-panic": {
      "suggested_key": {
        "default": "Ctrl+Shift+K"
      },
      "description": "Toggle Panic Button with Ctrl+Shift+K"
    }
  }
}
```
### Options.html

```html
<!DOCTYPE html>
<html>
<head>
  <title>Panic Button Options</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 10px;
    }
  </style>
  <script src="options.js"></script>
</head>
<body>
    <h1>Panic Button Options</h1>
    <form id="optionsForm">
    <label for="safeWebsiteInput">Safe Website URL:</label>
    <input type="text" id="safeWebsiteInput" name="safeWebsite" placeholder="Enter safe website URL">
    <br>
    <button type="submit">Save</button>
    <div id="confirmationMessage" style="display: none; color: green;"></div>

    </form>
</body>
</html>
```

### Options.js
```js
document.addEventListener('DOMContentLoaded', function() {
  const optionsForm = document.getElementById('optionsForm');
  const safeWebsiteInput = document.getElementById('safeWebsiteInput');

  // Load the saved safe website URL from storage
  chrome.storage.sync.get(['safeWebsite'], function(result) {
    if (result.safeWebsite) {
      safeWebsiteInput.value = result.safeWebsite;
    }
  });

  optionsForm.addEventListener('submit', function(event) {
    event.preventDefault();

    // Get the entered safe website URL
    const safeWebsite = safeWebsiteInput.value;

    // Save the safe website URL to storage
    chrome.storage.sync.set({ safeWebsite: safeWebsite }, function() {
      console.log('Safe website URL saved:', safeWebsite);

      // Send a message to the background script indicating that the safe website URL has been updated
      chrome.runtime.sendMessage({ action: 'safeWebsiteUpdated', url: safeWebsite });

      // Show confirmation message
    const confirmationMessage = document.getElementById('confirmationMessage');
    confirmationMessage.textContent = 'Safe website URL saved!';
    confirmationMessage.style.display = 'block';

    // Clear the confirmation message after 3 seconds
    setTimeout(function() {
      confirmationMessage.style.display = 'none';
    }, 3000);
    });
  });
});
```

### Background.js
```js
let isPanicModeActive = false;
let originalWindowState = null;
let originalWindowId = null;
let safeWindowId = null;
let safeWebsite = "";

chrome.commands.onCommand.addListener(function (command) {
  if (command === "toggle-panic") {
    if (isPanicModeActive) {
      // Close the safe window and restore the original window state
      if (safeWindowId) {
        chrome.windows.remove(safeWindowId, function () {
          safeWindowId = null;
          if (originalWindowState === "minimized") {
            chrome.windows.update(originalWindowId, { state: "minimized" });
          } else {
            chrome.windows.update(originalWindowId, { state: originalWindowState });
          }
        });
      }
      isPanicModeActive = false;
    } else {
      // Minimize or save the original window state and open the safe website in a new window
      chrome.windows.getCurrent(function (currentWindow) {
        originalWindowId = currentWindow.id;
        originalWindowState = currentWindow.state;
        if (originalWindowState === "minimized") {
          chrome.windows.update(originalWindowId, { state: "minimized" });
        } else {
          chrome.windows.update(originalWindowId, { state: "normal" });
        }
        chrome.windows.create({ url: safeWebsite, state: "maximized" }, function (newWindow) {
          safeWindowId = newWindow.id;
        });
      });

      isPanicModeActive = true;
    }
  }
});

// Listen for safe website URL updates from options.js
chrome.runtime.onMessage.addListener(function (message, sender, sendResponse) {
  if (message.action === 'safeWebsiteUpdated') {
    // Update the safe website URL
    safeWebsite = message.url;
    console.log('Safe website URL updated:', safeWebsite);
  }
});
```