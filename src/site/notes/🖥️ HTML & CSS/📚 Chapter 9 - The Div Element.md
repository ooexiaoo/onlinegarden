---
{"banner":"![florian-olivo-4hbJ-eymZ1o-unsplash.jpg](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/florian-olivo-4hbJ-eymZ1o-unsplash.jpg)","dg-publish":true,"permalink":"/html-and-css/chapter-9-the-div-element/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-11-14T21:08:36.656+05:30","updated":"2023-12-12T07:36:14.434+05:30"}
---

🧶 Tags - #HTML_CSS 

---
 Resources - [[]]
 
---
 Links - https://github.com/SuperSimpleDev/html-css-course-2022/tree/main/1-exercise-solutions/lesson-09
 
---
This is one of the most important elements in HTML. The div elements stands for division, or you can just call it a box.

* The div element by default is a block element.
* Div can contain any other elements inside.
* Div's are meant to be containers.

# Exercise 9a-9f -

![Screenshot_1 10.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2010.png)

# HTML
```
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

<link rel="stylesheet" href="exercise9.css">

</head>

<body>

<div class="redbox"></div>

<div class="greencircle"></div>

<div class="service">

<p>Satisfied with our service?</p>

<button>Yes</button>

<button>No</button>

</div>

<div class="youtube">

<p class="yt">Install YouTube Music</p>

<p class="para">Add YouTube Music to your desktop for

quick and easy access</p>

</div>

<div class="cat-tweet">

<img class="logo" src="/Exercise7/images/wp5208206-cute-anime-girl-hd-wallpapers.jpg">

<input class="tweet" type="text" placeholder="What's happening?">

<button class="tweet-button">Tweet</button>

</div>

<div class="catfb">

<img class="logo1" src="/Exercise7/images/wp5208206-cute-anime-girl-hd-wallpapers.jpg">

<p class="name">Oliver</p>

<p class="mutual">2 mutual friends</p>

<button class="friend-button">Add Friend</button>

</div>

</body>

</html>
```

# CSS
```
.redbox{

display: inline-block;

background-color: red;

width: 100px;

height: 100px;

margin-right: 15px;

}

.greencircle{

background-color: green;

width: 100px;

height: 100px;

border-radius: 50px;

display: inline-block;

}

.service{

display: inline-block;

margin: 10px;

padding: 15px;

width: 300px;

border: 1px solid black;

}

.youtube{

width: 370px;

display: inline-block;

padding-left: 20px;

padding-right: 20px;

background-color: rgb(43, 43, 43);

}

.yt{

line-height: 0px;

font-size: 25px;

font-weight: bold;

color: white;

}

.para{

color: rgb(153, 153, 153);

}

.cat-tweet{

vertical-align: middle;

margin: 5px;

display: inline-block;

padding: 10px;

box-shadow: 0 1px 3px rgb(82, 82, 82);

border-radius: 5px;

margin: 20px;

}

.logo{

vertical-align: middle;

width: 50px;

height: 50px;

border-radius: 50px;

margin-right: 3px;

}

.tweet{

border: none;

vertical-align: middle;

font-size: 20px;

margin-left: 3px;

}

.tweet-button{

padding-top: 8px;

padding-bottom: 8px;

padding-right: 15px;

padding-left: 15px;

border-radius: 50px;

border: none;

background-color: rgb(0, 110, 255);

color: white;

font-weight: bold;

}

.catfb{

margin-left: 20px;

width: 250px;

box-shadow: 0 1px 5px rgba(29, 29, 29, 0.3);

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

.mutual{

margin-top: 0;

margin-left: 8px;

color: gray;

margin-bottom: 10px;

}

.friend-button{

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
```

# Exercise 9g -

![Screenshot_1 11.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2011.png)
![Screenshot_1 12.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2012.png)

# HTML
```
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>9f</title>

<link rel="stylesheet" href="exerise9g.css">

</head>

<body>

<div class="catfb">

<img class="logo1" src="/9g/bgkawaii.jpg">

<p class="name">Olivia</p>

<p class="mutual">5 mutual friends</p>

<button class="friend-button">Add Friend</button>

</div>

<div class="catfb">

<img class="logo1" src="/9g/anime-girls-big-boobs.jpg">

<p class="name">Alisa</p>

<p class="mutual">2 mutual friends</p>

<button class="friend-button">Add Friend</button>

</div>

<div class="catfb">

<img class="logo1" src="/9g/digital-digital-art-illustration-artwork-eyes-closeup-2157607-wallhere.com.jpg">

<p class="name">Reina</p>

<p class="mutual">6 mutual friends</p>

<button class="friend-button">Add Friend</button>

</div>

<div class="google"><img class="logo" src="/purepng.com-google-logo-2015brandlogobrand-logoiconssymbolslogosgoogle-6815229372333mqrr.png"></div>

<div class="s"><input class="search" type="text" placeholder="Search Google or type a URL"></div>

<div class="g">

<button class="gg">Google Search</button>

<button class="gg">I'm Feeling Lucky</button>

</div>

</body>

</html>
```

# CSS
```
.catfb{

display: inline-block;

margin-left: 20px;

width: 250px;

box-shadow: 0 1px 5px rgba(29, 29, 29, 0.3);

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

.mutual{

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

.inline{

margin: 5px;

display: inline-block;

}

.logo{

width: 200px;

margin-bottom: 10px;

}

.search{

font-size: 15px;

padding-left: 10px;

padding-right: 100px;

padding-top: 10px;

padding-bottom: 10px;

border: none;

border-radius: 50px;

width: 300px;

box-shadow: 0 1px 5px rgb(122, 122, 122);

}

.google{

text-align: center;

margin-top: 20px;

}

.s{

text-align: center;

}

.g{

margin: 25px;

text-align: center;

}

.gg{

background-color: rgb(236, 236, 236);

padding-left: 20px;

padding-right: 20px;

padding-top: 10px;

padding-bottom: 10px;

border: none;

margin: 4px;

}
```