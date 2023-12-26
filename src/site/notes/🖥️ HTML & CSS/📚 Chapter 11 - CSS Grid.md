---
{"banner":"![florian-olivo-4hbJ-eymZ1o-unsplash.jpg](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/florian-olivo-4hbJ-eymZ1o-unsplash.jpg)","dg-publish":true,"permalink":"/html-and-css/chapter-11-css-grid/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-11-14T21:08:36.634+05:30","updated":"2023-12-12T07:36:39.285+05:30"}
---

🧶 Tags - #HTML_CSS 

---
Resources - [[]]
 
---
Links - https://github.com/SuperSimpleDev/html-css-course-2022/tree/main/1-exercise-solutions/lesson-11
 
# [[🖥️ HTML & CSS/📚 Chapter 11 - CSS Grid\|📚 Chapter 11 - CSS Grid]]
==2022-11-08 - 15:58==

Using CSS Grid is a much better way to create layouts than making DIVs. DIVs create spaces in between two DIV tags when we go to another line. This creates alignment issues -
```CSS
<div>{THERE IS A SPACE HERE}
	<div class="test" img="source.jpg">
</div>
```

## Inline Styles
To counteract this issue, we'll learn a better technique called CSS Grid. We can do this by writing our CSS inside HTML itself -
```
<div style="background-color: lightblue">div1</div>
```

The style element inside the DIV is a CSS element that can be used to style the DIV. This is known as <mark style="background: #FF5582A6;">inline styles</mark>.

So to create a grid, we use the main div and add these elements to it -

![Screenshot_1 14.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2014.png)

```
<div style="

display: grid;

grid-template-columns: 100px 100px;

">
```

* By using CSS grid, the sub DIVs automatically turn to inline-blocks, i.e, they don't take the entire line.
* There are no gaps created inside grids, which is the problem with just using DIVs.
* When you add more elements inside the sub DIV it makes it taller but keeps everything vertically aligned.
* If you add more columns than specified, it'll wrap around to the row below.

## Free Space
When adding the dimensions of the row, you can also use the value called <mark style="background: #FF5582A6;">fr</mark> or Free Space.

![Screenshot_1 15.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2015.png)

* Fr value can also be used as ratios.
```
<div style="

margin-top: 30px;

display: grid;

grid-template-columns: 100px 1fr 2fr;

">
```
---
# Example

![Screenshot_1 16.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2016.png)

```HTML
<!DOCTYPE html>

<html>

<head>

<title>Youtube.com Clone</title>

<link rel="preconnect" href="https://fonts.googleapis.com">

<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700;900&display=swap" rel="stylesheet">

<Style>

p{

font-family: roboto, arial;

margin-top: 0;

margin-bottom: 0;

}

.thumbnail{

width: 100%;

}

.search-bar{

font-size: 20px;

margin-left: 12px;

display: block;

}

.preview{

}

.profile-pic{

width: 40px;

border-radius: 50px;

}

.video-title{

font-size: 14px;

font-weight: 500;

margin-top: 0;

line-height: 20px;

margin-bottom: 12px;

}

.thumbnail-row{

margin-bottom: 12px;

}

.author,

.view {

font-size: 12px;

color: rgb(96,96,96);

}

.author{

margin-bottom: 4px;

}

.video-info-grid{

display:grid;

grid-template-columns: 50px 1fr;

}

.video-grid{

display: grid;

grid-template-columns: 1fr 1fr 1fr;

column-gap: 16px;

row-gap: 40px;

}

</Style>

</head>

<body>

<input class="search-bar" type="text" placeholder="search">

<div class="video-grid">

<div class="preview">

<div class="thumbnail-row">

<img class="thumbnail" src="Thumbnails/thumbnail-1.webp">

</div>

<div class="video-info-grid">

<div class="channel-pic">

<img class="profile-pic" src="/Intro-to-html/Channel Pics/channel-1.jpeg">

</div>

<div class="video-info">

<p class="video-title">

Talking Tech and AI with Google CEO Sundar Pichai!

</p>

<p class="author">

Marques Brownlee

</p>

<p class="view">

3.4M views &#183; 6 months ago

</p></div>

</div>

</div>

<div class="preview">

<div class="thumbnail-row">

<img class="thumbnail" src="Thumbnails/thumbnail-2.webp">

</div>

<div class="video-info-grid">

<div class="channel-pic">

<img class="profile-pic" src="/Intro-to-html/Channel Pics/channel-2.jpeg">

</div>

<div class="video-info">

<p class="video-title">

Try Not To Laugh Challenge #9

</p>

<p class="author">

Markiplier

</p>

<p class="view">

19M views &#183; 4 years ago

</p></div>

</div>

</div>

<div class="preview">

<div class="thumbnail-row">

<img class="thumbnail" src="Thumbnails/thumbnail-3.webp">

</div>

<div class="video-info-grid">

<div class="channel-pic">

<img class="profile-pic" src="/Intro-to-html/Channel Pics/channel-3.jpeg">

</div>

<div class="video-info">

<p class="video-title">

Crazy Tik Toks Taken Moments Before DISASTER

</p>

<p class="author">

SSSniperWolf

</p>

<p class="view">

12M views · 1 year ago

</p></div>

</div>

</div>

<div class="preview">

<div class="thumbnail-row">

<img class="thumbnail" src="Thumbnails/thumbnail-4.webp">

</div>

<div class="video-info-grid">

<div class="channel-pic">

<img class="profile-pic" src="/Intro-to-html/Channel Pics/channel-4.jpeg">

</div>

<div class="video-info">

<p class="video-title">

The Simplest Math Problem No One Can Solve - Collatz Conjecture

</p>

<p class="author">

Veritasium

</p>

<p class="view">

18M views · 4 months ago

</p></div>

</div>

</div>

<div class="preview">

<div class="thumbnail-row">

<img class="thumbnail" src="Thumbnails/thumbnail-5.webp">

</div>

<div class="video-info-grid">

<div class="channel-pic">

<img class="profile-pic" src="/Intro-to-html/Channel Pics/channel-5.jpeg">

</div>

<div class="video-info">

<p class="video-title">

Kadane's Algorithm to Maximum Sum Subarray Problem

</p>

<p class="author">

CS Dojo

</p>

<p class="view">

519K views · 5 years ago

</p></div>

</div>

</div>

<div class="preview">

<div class="thumbnail-row">

<img class="thumbnail" src="Thumbnails/thumbnail-6.webp">

</div>

<div class="video-info-grid">

<div class="channel-pic">

<img class="profile-pic" src="/Intro-to-html/Channel Pics/channel-6.jpeg">

</div>

<div class="video-info">

<p class="video-title">

Anything You Can Fit In The Circle I&#39;ll Pay For

</p>

<p class="author">

MrBeast

</p>

<p class="view">

141M views · 1 year ago

</p></div>

</div>

</div>

</div>

</body>

</html>
```
---
# Exercise 11a-11c -

![Screenshot_3.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_3.png)

# HTML -
```
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>CSS GRID LESSON</title>

<link rel="stylesheet" href="EXERCISE11.css">

</head>

<body>

<div class="video-columns">

<p class="aa">200px</p>

<p class="ab">75px</p>

</div>

<div class="column2">

<p class="ab">col1</p>

<p class="aa">col2</p>

<p class="ab">col3</p>

</div>

<div class="column3">

<p class="ac">col1</p>

<p class="ac">col2</p>

<p class="ac">col3</p>

<p class="ac">col4</p>

<p class="ac">col1</p>

<p class="ac">col2</p>

<p class="ac">col3</p>

<p class="ac">col4</p>

</div>

</body>

</html>
```

# CSS -
```
*{

font-family: Arial, Helvetica, sans-serif;

}

.video-columns{

display: grid;

grid-template-columns: 200px 75px;

}

.aa{

background-color: lightblue;

}

.ab{

background-color: lightpink;

}

.column2{

display: grid;

grid-template-columns: 50px 1fr 75px;

}

.column3{

display: grid;

grid-template-columns: 1fr 1fr 1fr 1fr;

column-gap: 20px;

row-gap: 10px;

}

.ac{

margin: 0;

background-color: lightpink;

}
```
---
# Exercise 11d -

![Screenshot_1 17.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2017.png)

# HTML -
```
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>9f</title>

<link rel="stylesheet" href="exercise11d.css">

</head>

<body>

<div class="cat">

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

</div>

</body>

</html>
```

# CSS -
```
.cat{

display: grid;

grid-template-columns: 250px 250px 250px;

column-gap: 20px;

}

.catfb{

width: 250px;

margin-top: 20px;

margin-left: 20px;

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

height: 28px;

width: 28px;

object-fit: cover;

border-radius: 14px;

vertical-align: middle;

margin-right: 4px;

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

  

.mutuald{

margin-left: 8px;

margin-bottom: 10px;

display: grid;

grid-template-columns: 28px 1fr;

}
```
---
