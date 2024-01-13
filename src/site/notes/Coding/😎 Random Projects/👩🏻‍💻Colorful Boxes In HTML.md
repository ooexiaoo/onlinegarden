---
{"dg-publish":true,"permalink":"/coding/random-projects/colorful-boxes-in-html/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-11-14T21:08:36.714+05:30","updated":"2024-01-13T12:22:14.441+05:30"}
---

🧶 Tags:: #HTML #Random_Projects
==2022-10-13 - 04:26==

### HTML Code

```HTML
<!DOCTYPE html>

<html lang="en">

  <head>

    <meta charset="UTF-8" />

    <meta http-equiv="X-UA-Compatible" content="IE=edge" />

    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <title>Document</title>

    <link rel="stylesheet" href="style.css" />

    <script src="app.js" defer></script>

  </head>

  <body>

    <div class="container" id="container"></div>

  </body>

</html>
```
### STYLE.CSS
```CSS
* {

    box-sitting:border-box

}

body{

    background-color: #111;

    display: flex;

    align-items: center;

    justify-content: center;

    height: 100vh;

    overflow: hidden;

    margin: 0;

}

  

.container {

    display: flex;

    align-items: center;

    justify-content: center;

    flex-wrap: wrap;

    max-width: 1600px;

  

}

  

.square {

    background-color: #1d1d1d;

    box-sizing: 0 0 2px black;

    height: 50px;

    width: 50px;

    margin: 2px;

    transition: 2s ease;

}

  

.square:hover {

    transition-duration: 0s;

  

}
```

### APP.JS
```JavaScript
const container = document.getElementById('container')

const colors = ['#e74c4c', '#8e44ad', '#3498db', '#e67e22', '#2ecc71']

const SQUARES = 522

  

for(let i = 0; i < SQUARES; i++) {

    const square = document.createElement('div')

    square.classList.add('square')

  

    square.addEventListener('mouseover', () => setColor(square))

    square.addEventListener('mouseout', () => removeColor(square))

  

    container.appendChild(square)

}

  

function setColor(element) {

    const color = getRandom()

    element.style.background = color

    element.style.boxShadow = '0 0 2px ${color}, 0 0 10px $(color)'

}

  
  

function removeColor(element) {

    element.style.background = '#1d1d1d'

    element.style.boxShadow = '0 0 2px #000'

}

  

function getRandom() {

    return colors[Math.floor(Math.random() * colors.length)]

}
```
