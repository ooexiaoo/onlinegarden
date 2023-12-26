---
{"banner":"![florian-olivo-4hbJ-eymZ1o-unsplash.jpg](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/florian-olivo-4hbJ-eymZ1o-unsplash.jpg)","dg-publish":true,"permalink":"/html-and-css/chapter-10-nested-layouts-technique/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-11-14T21:08:36.593+05:30","updated":"2023-12-26T20:43:03.677+05:30"}
---

🧶 Tags:: #HTML_CSS 
🗃 Resources:: [[]]
 Links:: https://github.com/SuperSimpleDev/html-css-course-2022/tree/main/1-exercise-solutions/lesson-10
 
---
![Pasted image 20221107143326.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Pasted%20image%2020221107143326.png)

# Exercise 10d -

![Screenshot_1 13.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2013.png)

# HTML -

```
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>9f</title>

<link rel="stylesheet" href="exercise10.css">

</head>

<body>

<div class="catfb">

<img class="logo1" src="/9g/bgkawaii.jpg">

<div class="named">

<p class="name">Olivia</p>

</div>

<div class="mutuald">

<img class="test" src="/9g/1.1.99_19063.jpg">

<p class="mutual">5 mutual friends</p>

</div>

<div class="buttond">

<button class="friend-button">Add Friend</button>

</div>

</div>

<div class="catfb">

<img class="logo1" src="/9g/anime-girls-big-boobs.jpg">

<div class="named">

<p class="name">Alisa</p>

</div>

<div class="mutuald">

<img class="test" src="/9g/1.1.99_19063.jpg">

<p class="mutual">2 mutual friends</p>

</div>

<div class="buttond">

<button class="friend-button">Add Friend</button>

</div>

</div>

<div class="catfb">

<img class="logo1" src="/9g/digital-digital-art-illustration-artwork-eyes-closeup-2157607-wallhere.com.jpg">

<div class="named">

<p class="name">Reina</p>

</div>

<div class="mutuald">

<img class="test" src="/9g/1.1.99_19063.jpg">

<p class="mutual">6 mutual friends</p>

</div>

<div class="buttond">

<button class="friend-button">Add Friend</button>

</div>

</div>

</body>

</html>
```

# CSS -

```
.catfb{

margin-top: 20px;

display: inline-block;

margin-left: 20px;

width: 250px;

box-shadow: 0 1px 5px rgba(29, 29, 29, 1);

}

.logo1{

object-fit: cover;

width: 250px;

height: 250px;

  

}

.name{

line-height: 0px;

margin-left: 8px;

font-weight: bold;

font-size: 20px;

}

.test{

display: inline-block;

height: 28px;

width: 28px;

object-fit: cover;

border-radius: 14px;

vertical-align: middle;

margin-right: 4px;

}

.mutual{

display: inline-block;

margin-top: 0;

margin-left: 8px;

color: gray;

margin-bottom: 10px;

}

.friend-button{

cursor: pointer;

padding-left: 20px;

padding-right: 20px;

padding-top: 10px;

padding-bottom: 10px;

background-color: rgb(0, 140, 255);

color: white;

border: none;

border-radius: 3px;

margin-left: 8px;

margin-bottom: 8px;

}

  

.mutuald{

margin-left: 8px;

margin-bottom: 10px;

display: inline-block;

}
```