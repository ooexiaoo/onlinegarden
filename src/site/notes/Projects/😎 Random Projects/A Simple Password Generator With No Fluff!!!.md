---
{"dg-publish":true,"permalink":"/projects/random-projects/a-simple-password-generator-with-no-fluff/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-12-27T20:24:57.461+05:30","updated":"2023-12-29T17:11:06.584+05:30"}
---

Tags:: #HTML_CSS #JavaScript 
==2023-12-27 | 21:27==

Check out the [password generator here](https://simplepass.pages.dev/).
I wanted to create a simple password generator that can generate long passwords quickly.

![Simplepass.webp](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Simplepass.webp)

### The UI is extremely simple to use:
- Just use the slider to select the length of the password.
- Check or uncheck what you want in your passwords - **Uppercase, Lowercase, Numbers, Special Characters**.
- If you don't like the password that you see, just keep clicking **Generate password** to generate a new password with the same parameters you've selected.
- Quickly copy your passwords with the copy button.
- Create up to 128 character long passwords.

I've already made a [[Projects/Name Unavailable/Random Password Generator\|password generating extension]], but I thought most people wouldn't really want to install an extension that just generates passwords. It's like installing an app just to see use a webpage.

So this is the better option overall.

## Enjoy!

Even though you can find all the code at GitHub, I've also provided the code here as well.
### Here is All the Code:
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta charset="UTF-8">
  <title>Password Generator</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <h1>Password Generator</h1>
    <div>
      <label for="lengthRange">Password Length:</label>
      <input type="range" min="1" max="128" value="64" id="lengthRange">
      <span id="lengthValue">8</span>
    </div>
    <div>
      <label for="uppercaseCheck">Include Uppercase:</label>
      <input type="checkbox" id="uppercaseCheck">
    </div>
    <div>
      <label for="lowercaseCheck">Include Lowercase:</label>
      <input type="checkbox" id="lowercaseCheck" checked>
    </div>
    <div>
      <label for="numbersCheck">Include Numbers:</label>
      <input type="checkbox" id="numbersCheck" checked>
    </div>
    <div>
      <label for="specialCharsCheck">Include Special Characters:</label>
      <input type="checkbox" id="specialCharsCheck">
    </div>
    <button id="generateBtn">Generate Password</button>
    <div>
      <input type="text" id="passwordOutput" readonly>
      <button id="copyBtn">Copy Password</button>
    </div>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

```CSS
body {
    font-family: Arial, sans-serif;
    background-color: #ffff00;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
  }
  
  .container {
    width: 60%;
    max-width: 550px;
    text-align: center;
    padding: 20px;
    background-color: rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  
  h1 {
    margin-bottom: 20px;
  }
  
  input[type="range"] {
    width: 80%;
  }
  
  input[type="text"] {
    width: 80%;
    margin-top: 10px;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  button {
    margin-top: 10px;
    padding: 8px 16px;
    cursor: pointer;
    border-radius: 4px;
    border: none;
    background-color: #66fa7f;
    color: #fff;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  
  #copyBtn {
    margin-left: 10px;
  }
  
  @media screen and (max-width: 768px) {
    .container {
      width: 80%; /* Adjust width for smaller screens */
      padding: 10px; /* Adjust padding for smaller screens */
    }
  
    input[type="range"],
    input[type="text"] {
      width: 100%; /* Full width for input elements on smaller screens */
    }
  }
```

```JavaScript
document.addEventListener('DOMContentLoaded', function () {
    const lengthRange = document.getElementById('lengthRange');
    const lengthValue = document.getElementById('lengthValue');
    const uppercaseCheck = document.getElementById('uppercaseCheck');
    const lowercaseCheck = document.getElementById('lowercaseCheck');
    const numbersCheck = document.getElementById('numbersCheck');
    const specialCharsCheck = document.getElementById('specialCharsCheck');
    const generateBtn = document.getElementById('generateBtn');
    const passwordOutput = document.getElementById('passwordOutput');
    const copyBtn = document.getElementById('copyBtn');
  
    lengthRange.addEventListener('input', function () {
      lengthValue.textContent = lengthRange.value;
      generatePassword();
      changeBackgroundColor();
    });
  
    generateBtn.addEventListener('click', function () {
      generatePassword();
      changeBackgroundColor();
    });
  
    copyBtn.addEventListener('click', function () {
      passwordOutput.select();
      document.execCommand('copy');
      alert('Password copied to clipboard!');
    });
  
    uppercaseCheck.addEventListener('change', function () {
      generatePassword();
    });
  
    lowercaseCheck.addEventListener('change', function () {
      generatePassword();
    });
  
    numbersCheck.addEventListener('change', function () {
      generatePassword();
    });
  
    specialCharsCheck.addEventListener('change', function () {
      generatePassword();
    });
  
    function generatePassword() {
      const length = lengthRange.value;
      const uppercase = uppercaseCheck.checked;
      const lowercase = lowercaseCheck.checked;
      const numbers = numbersCheck.checked;
      const specialChars = specialCharsCheck.checked;
      const charset = generateCharset(uppercase, lowercase, numbers, specialChars);
  
      let password = '';
      for (let i = 0; i < length; i++) {
        const randomIndex = Math.floor(Math.random() * charset.length);
        password += charset[randomIndex];
      }
  
      passwordOutput.value = password;
    }
  
    function generateCharset(uppercase, lowercase, numbers, specialChars) {
      let charset = '';
      if (uppercase) charset += 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
      if (lowercase) charset += 'abcdefghijklmnopqrstuvwxyz';
      if (numbers) charset += '0123456789';
      if (specialChars) charset += '!@#$%^&*()_+-=[]{}|;:,.<>?';
  
      return charset;
    }
  
    function changeBackgroundColor() {
      const passwordStrength = getPasswordStrength();
      let backgroundColor;
    
      const color1 = [255, 153, 153]; // Red for weak passwords
      const color2 = [255, 255, 0]; // Yellow for medium passwords
      const color3 = [153, 255, 153]; // Green for strong passwords
    
      const maxLength = 128;
      const minLength = 1;
    
      // Calculate the interpolation value between 0 and 1 based on password length
      let interpolation = (passwordStrength - minLength) / (maxLength - minLength);
    
      // Ensure interpolation value is within the range of 0 to 1
      interpolation = Math.min(Math.max(interpolation, 0), 1);
    
      // Interpolate between colors based on the interpolation value
      if (interpolation <= 0.5) {
        backgroundColor = interpolateColor(color1, color2, interpolation * 2);
      } else {
        backgroundColor = interpolateColor(color2, color3, (interpolation - 0.5) * 2);
      }
    
      document.body.style.transition = 'background-color 0.5s ease-in-out';
      document.body.style.backgroundColor = `rgb(${backgroundColor[0]}, ${backgroundColor[1]}, ${backgroundColor[2]})`;
    }
    
    // Interpolate between two colors based on a given ratio
    function interpolateColor(color1, color2, ratio) {
      const result = [];
      for (let i = 0; i < 3; i++) {
        result.push(Math.round(color1[i] * (1 - ratio) + color2[i] * ratio));
      }
      return result;
    }
    
    function getPasswordStrength() {
      const password = passwordOutput.value;
      const length = password.length;
      return length;
    }
    
  });
```