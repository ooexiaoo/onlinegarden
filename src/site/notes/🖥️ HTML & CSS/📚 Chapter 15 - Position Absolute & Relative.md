---
{"banner":"![florian-olivo-4hbJ-eymZ1o-unsplash.jpg](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/florian-olivo-4hbJ-eymZ1o-unsplash.jpg)","dg-publish":true,"permalink":"/html-and-css/chapter-15-position-absolute-and-relative/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-11-14T21:08:36.673+05:30","updated":"2023-12-26T20:44:58.264+05:30"}
---

🧶 Tags:: #HTML_CSS 
🗃 Resources:: [[]]
==2022-11-12 - 22:33==

## Position: absolute;
 Even though position absolute behaves similar to <mark style="background: #FF5582A6;">position fixed</mark>. There is just one key difference, while for position fixed the elements are placed in the browser window. While for position absolute, they are placed on the page.

 ### Fixed = Placed in the <mark style="background: #FFF3A3A6;">browser window</mark>
 ### Absolute = placed on the <mark style="background: #FFF3A3A6;">page</mark>
---
## Position: relative;
Position relative makes it possible to display other elements in a relative size to the place where it's placed in.

So, if you place a number inside an image <mark style="background: #FF5582A6;">eg. 'left:10px;'</mark>. The number will be placed relative to the image and not the page. So when you scroll the page the number will stay in the same place in the image.
![Screenshot_1 27.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2027.png)
---
# Exercise 15a-15d -
![Screenshot_1 28.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2028.png)

# HTML -
```
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Position Absolute/Relative</title>

<link rel="stylesheet" href="exercise15a15c.css">

</head>

<body>

<div class="close">

X

</div>

<div class="box">

<div class="close-floating">

X

</div>

<div class="time">

0:29

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

.close{

position: absolute;

background-color: black;

color: white;

padding-left: 15px;

padding-right: 15px;

padding-top: 10px;

padding-bottom: 10px;

border-radius: 50px;

right: 10px;

top: 10px;

}

.box{

width: 320px;

height: 180px;

background-color: gray;

position: fixed;

bottom: 10px;

right: 10px;

}

.close-floating{

position: absolute;

background-color: black;

color: white;

padding-left: 15px;

padding-right: 15px;

padding-top: 10px;

padding-bottom: 10px;

border-radius: 50px;

left: -15px;

top: -15px;

}

.time{

background-color: black;

color: white;

position: absolute;

bottom: 10px;

right: 10px;

padding-right: 5px;

padding-left: 5px;

padding-top: 2px;

padding-bottom: 2px;

border-radius: 3px;

}
```
---
# Exercise 15e-15f -
![Screenshot_1 29.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2029.png)

# HTML -
```
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Position Absolute/Relative</title>

<link rel="stylesheet" href="exercise15e15f.css">

</head>

<body>

<div class="store">

<img class="image" src="tops-t-shirt-men-anime-girl-fit-inscriptions-4066589790.jpg">

<div class="discount">

20% OFF

</div>

<div class="option">

<button class="atc">

Add To Cart

</button>

</div>

</div>

</body>

</html>
```

# CSS -
```
body{

background-color:bisque;

height: 3000px;

}

.store{

margin-top: 50px;

margin-left: 25px;

position: relative;

display: inline-block;

}

.image{

height: 250px;

width: 250px;

}

.discount{

position: absolute;

top: 10px;

right: 0;

background-color: black;

color: white;

padding-right: 5px;

padding-left: 5px;

padding-top: 2px;

padding-bottom: 2px;

font-size: 14px;

}

.option{

position: absolute;

background-color: rgba(228, 228, 228, 0.5);

bottom: 0;

right: 0;

left: 0;

top: 180px;

justify-content: center;

align-items: center;

display: flex;

}

.atc{

position: absolute;

background-color: white;

border: solid;

border-width: 2px;

padding-top: 6px;

padding-bottom: 6px;

padding-right: 8px;

padding-left: 8px;

font-weight: 500;

margin: 0;

}
```