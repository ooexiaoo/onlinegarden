---
{"dg-publish":true,"permalink":"/projects/name-unavailable/random-password-generator/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-11-14T21:08:36.733+05:30","updated":"2023-12-12T00:56:36.383+05:30"}
---

🧶 Tags - #Random_Projects 

---
🗃 Resources - [[]]

# [[Projects/Name Unavailable/Random Password Generator\|Random Password Generator]]
==2023-06-18 - 19:48==

---
Wanted to try creating a random password generator so, I did!

It mainly uses Random Math Floor to come up with just random things that can be used as a password.

I want to try to add Anime names to it if I can, just for fun. If I can get a list of anime names list, I will.

The whole project is <mark style="background: #BBFABBA6;">99KiB</mark> Including the images. Pretty Light, Pretty Nice!

You can find the project on by clicking here - [Github.com](https://github.com/ooexiaoo/Password-Generator-Extension).

![1.webp](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/1.webp)

## Here's The Code:
### JSON
```JSON
{
    "manifest_version": 2,
    "name": "Password Generator",
    "description": "A simple Password Generator"
    "version": "1.0",
    "description": "Generate strong passwords.",
    "permissions": ["clipboardWrite"],
    "browser_action": {
      "default_popup": "popup.html"
    },
    "icons": {
      "16": "icon.png",
      "48": "icon.png",
      "128": "icon.png"
    }
  }
```
### HTML
```HTML
<!DOCTYPE html>
<html>
<head>
  <title>Password Generator</title>
  <script src="popup.js"></script>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Password Generator</h1>
  <div>
    <label>Length: </label>
    <input type="number" id="lengthInput" min="6" max="32" value="12">
  </div>
  <div>
    <label>Include Uppercase: </label>
    <input type="checkbox" id="uppercaseCheckbox" checked>
  </div>
  <div>
    <label>Include Lowercase: </label>
    <input type="checkbox" id="lowercaseCheckbox" checked>
  </div>
  <div>
    <label>Include Numbers: </label>
    <input type="checkbox" id="numbersCheckbox" checked>
  </div>
  <div>
    <label>Include Special Characters: </label>
    <input type="checkbox" id="specialCharsCheckbox" checked>
  </div>
  <div>
    <button id="generateButton">Generate Password</button>
    <button id="copyButton">Copy Password</button>
  </div>
  <div>
    <label for="passwordInput">Password:</label>
    <input type="text" id="passwordInput" readonly>
  </div>
</body>
</html>
```

### CSS
```CSS
body {
    font-family: Arial, sans-serif;
    background-color: #333;
    padding: 20px;
    color: #fff;
  }
  
  h1 {
    color: #fff;
  }
  
  .container {
    max-width: 400px;
    margin: 0 auto;
  }
  
  .label {
    display: block;
    margin-bottom: 5px;
    color: #fff;
  }
  
  .input-group {
    margin-bottom: 10px;
  }
  
  .checkbox-label {
    display: inline-block;
    margin-right: 10px;
    color: #fff;
  }
  
  #generateButton,
  #copyButton {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    margin: 10px;
  }
  
  #copyButton {
    background-color: #008CBA;
  }
  
  #passwordInput {
    padding: 10px;
    max-width: 100%;
    background-color: #fff;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  #passwordInput:focus {
    outline: none;
    border-color: #008CBA;
  }
```

### POPUP.JS
```JS
// popup.js

document.addEventListener('DOMContentLoaded', function () {
    const generateButton = document.getElementById('generateButton');
    const copyButton = document.getElementById('copyButton');
  
    generateButton.addEventListener('click', generatePassword);
    copyButton.addEventListener('click', copyToClipboard);
  });
  
  function generatePassword() {
    const length = document.getElementById('lengthInput').value;
    const includeUppercase = document.getElementById('uppercaseCheckbox').checked;
    const includeLowercase = document.getElementById('lowercaseCheckbox').checked;
    const includeNumbers = document.getElementById('numbersCheckbox').checked;
    const includeSpecialChars = document.getElementById('specialCharsCheckbox').checked;
  
    const uppercaseChars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
    const lowercaseChars = 'abcdefghijklmnopqrstuvwxyz';
    const numberChars = '0123456789';
    const specialChars = '!@#$%^&*()_+~`|}{[]\\:;?><,./-=';
  
    let validChars = '';
    if (includeUppercase) validChars += uppercaseChars;
    if (includeLowercase) validChars += lowercaseChars;
    if (includeNumbers) validChars += numberChars;
    if (includeSpecialChars) validChars += specialChars;
  
    let password = '';
    for (let i = 0; i < length; i++) {
      const randomIndex = Math.floor(Math.random() * validChars.length);
      password += validChars.charAt(randomIndex);
    }
  
    const passwordInput = document.getElementById('passwordInput');
    passwordInput.value = password;
  }
  
  function copyToClipboard() {
    const passwordInput = document.getElementById('passwordInput');
    passwordInput.select();
    document.execCommand('copy');
  }
```

### POPUP-EVENT.JS
```JS
document.addEventListener('DOMContentLoaded', function () {
    const generateButton = document.getElementById('generateButton');
    const copyButton = document.getElementById('copyButton');
  
    generateButton.addEventListener('click', generatePassword);
    copyButton.addEventListener('click', copyToClipboard);
  });
  
  function generatePassword() {
    // The generatePassword function code remains the same
  }
  
  function copyToClipboard() {
    // The copyToClipboard function code remains the same
  }
```