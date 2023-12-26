---
{"banner":"![florian-olivo-4hbJ-eymZ1o-unsplash.jpg](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/florian-olivo-4hbJ-eymZ1o-unsplash.jpg)","dg-publish":true,"permalink":"/html-and-css/chapter-14-css-position/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-11-14T21:08:36.616+05:30","updated":"2023-12-12T07:37:04.114+05:30"}
---

🧶 Tags - #HTML_CSS 

---
🗃Resources - [[]]
 
---
🔗Links -
 
# [[🖥️ HTML & CSS/📚 Chapter 14 - CSS Position\|📚 Chapter 14 - CSS Position]]
==2022-11-11 - 15:24==
CSS position helps us do things like keep the header or the sidebar at the top of the page as we scroll. CSS position adds another dimension to our page, it's like another layer in Photoshop.

## Position: fixed;
When we add this property, the content remains in a fixed position even when we scroll the page. This can be used for headers or sidebars.

## Position: static;
This property made the content scrollable just like any other content on the screen.

## Top: 0px;
Using this property keeps the content at the top of the page. We can change the pixel value to the desired number.
The same way we can use left, right, or bottom property to make different headers or sidebars, etc.

One thing to note is that if we set the opposite properties, like left:50px; right:50px; The element will stretch to the desired values.

## Editing the YouTube Header
```CSS
.header{

position: fixed;

top: 0;

left: 0;

right: 0;

height: 55px;

display: flex;

flex-direction: row;

justify-content: space-between;

background-color: white;

border-bottom-width: 1px;

border-bottom-style: solid;

border-bottom-color: rgb(192,192,192)

}
```
![Screenshot_1 22.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2022.png)
---
## Created a Sidebar
![Screenshot_1 23.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2023.png)

```
.sidebar{

position: fixed;

left: 0;

bottom: 0;

top: 55px;

background-color: white;

width: 72px;

}
```

# Exercise 14a-14c -
![Screenshot_1 24.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2024.png)
# HTML -
```HTML
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Exercise 14</title>

<link rel="stylesheet" href="exerccise14a-14c.css">

</head>

<body>

<div class="bottom-right">

bottom-right

</div>

<div class="right-sidebar">

right-sidebar

</div>

<div class="modal">

<div class="box">

<p class="title">

Modal Title

</p>

<p class="para">

This is a modal

</p>

<button class="close-button">

close

</button>

</div>

</div>

</body>

</html>
```

# CSS -
```
body{

height: 3000px;

}

.bottom-right{

position: fixed;

background-color: black;

color: white;

bottom: 20px;

right: 20px;

z-index: 5;

}

.right-sidebar{

position: fixed;

background-color: green;

color: white;

right: 0;

width: 100px;

top: 0;

bottom: 0;

}

.modal{

display: flex;

position: fixed;

background-color: rgb(0,0,0,0.8);

top: 0;

bottom: 0;

left: 0;

right: 0;

align-items: center;

justify-content: center;

}

.box{

align-items: center;

background-color: white;

width: 400px;

height: fit-content;

border-radius: 10px;

}

.title{

padding-left: 15px;

font-size: 30px;

font-weight: bold;

margin-bottom: 2px;

}

.para{

padding-left: 15px;

margin-top: 2px;

font-size: 18px;

}

.close-button{

margin-left: 15px;

margin-bottom: 15px;

font-size: 16px;

}
```
---

# Exercise 14e-14f -
![Screenshot_1 26.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2026.png)
![Screenshot_1 25.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2025.png)

# HTML -
```
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Exercise 14e-14f

</title>

<link rel="stylesheet" href="exercise14e-14f.css">

</head>

<body>

<div class="header">

<div class="left-section">

<img class="profile-picture" src="/9g/1.1.99_19063.jpg">

<p class="name">

Miss Olivia

</p>

</div>

<div class="right-section">

<button class="friend">Add Friend</button>

<button class="message">Message</button>

</div>

</div>

<div class="discord">

<div class="pictures">

<img class="profile-pictures" src="/9g/anime-girls-big-boobs.jpg">

<img class="profile-pictures" src="/9g/1.1.99_19063.jpg">

<img class="profile-pictures" src="/9g/bgkawaii.jpg">

</div>

<div class="data">

<div class="info">

<p class="heading">

INFO

</p>

<P class="plus">+</P>

</div>

<div class="hashtags">

<p class="categories">

# new-videos

</p>

<p class="categories">

# updates

</p>

<p class="categories">

# faq

</p>

</div>

</div>

</div>

</body>

</html>
```

# CSS -
```
.header{

top: 0;

left: 0;

right: 0;

position: fixed;

display: flex;

width: 100%;

height: 50px;

flex-direction: row;

justify-content: space-between;

background-color: white;

}

.left-section{

display: flex;

justify-content: space-between;

vertical-align: middle;

align-items: center;

}

.right-section{

display: flex;

justify-content: space-between;

}

.profile-picture{

height: 40px;

width: 40px;

border-radius: 20px;

margin-left: 60px;

align-items: center;

}

.name{

margin-left: 10px;

margin-right: 10px;

font-weight: 500;

}

.right-section{

width: 250px;

align-items: center;

justify-content: left;

}

.friend{

background-color: rgb(0, 110, 255);

color: white;

border: none;

margin-right: 3px;

height: 30px;

margin-top: 15px;

margin-bottom: 15px;

align-items: center;

border-radius: 5px;

padding-left: 15px;

padding-right: 15px;

font-weight: bold;

}

.message{

background-color: rgb(228, 228, 228);

color: black;

border: none;

margin-left: 3px;

height: 30px;

margin-top: 15px;

margin-bottom: 15px;

align-items: center;

border-radius: 5px;

padding-left: 15px;

padding-right: 15px;

font-weight: bold;

}

body{

margin: 0;

padding-top: 50px;

}

.discord{

position: fixed;

top: 55px;

left: 0;

bottom: 0;

display: flex;

width: 250px;

background-color: rgb(48, 48, 48);

}

.pictures{

background-color: rgb(39, 39, 39);

width: 55px;

padding-left: 10px;

padding-right: 10px;

padding-top: 20px;

}

.profile-pictures{

height: 50px;

width: 50px;

border-radius: 25px;

margin: 5px;

}

.data{

}

.info{

display: flex;

justify-content: space-between;

width: 100%;

margin: 0;

}

.heading{

width: 130px;

color: white;

padding-left: 20px;

margin-top: 15px;

}

.plus{

color: gray;

font-size: 25px;

padding-right: 0;

margin-right: 0;

align-items: center;

margin-top: 15px;

}

.categories{

padding-left: 20px;

color: rgb(163, 163, 163);

}
```