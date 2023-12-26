---
{"banner":"![florian-olivo-4hbJ-eymZ1o-unsplash.jpg](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/florian-olivo-4hbJ-eymZ1o-unsplash.jpg)","dg-publish":true,"permalink":"/html-and-css/chapter-17-responsive-design/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-11-14T21:08:36.667+05:30","updated":"2023-12-26T20:45:18.153+05:30"}
---

🧶 Tags:: #HTML_CSS 
🗃 Resources:: [[]]
==2022-11-15 - 14:13==

## Media Query -
We can make a responsive design by creating a media query. This can be done by -
```
@media (mid-width: 75px) and (max-width : 999px){
video-grid{
	grid-template-columns: 1fr 1fr 1fr;
	}
}
```

---
## YouTube Example -
#### Screen size 750-999px
![Screenshot_1 31.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2031.png)
#### Anythingless than 750px
![Screenshot_1 32.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2032.png)
#### Anything more than 1000px
![Screenshot_2 5.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_2%205.png)

## HTML -
```
<!DOCTYPE html>

<html>

<head>

<title>Youtube.com Clone</title>

<link rel="preconnect" href="https://fonts.googleapis.com">

<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700;900&display=swap" rel="stylesheet">

<link rel="stylesheet" href="video.css">

<link rel="stylesheet" href="header.css">

<link rel="stylesheet" href="general.css">

<link rel="stylesheet" href="sidebar.css">

</head>

<body>

<div class="header">

<div class="left-section">

<img class="hamburger-menu"

src="/Intro-to-html/youtube/hamburger-menu.svg">

<img class="youtube-logo" src="/Intro-to-html/youtube/youtube-logo.svg">

</div>

<div class="middle-section">

<input class="search-bar" type="text" placeholder="search">

<button class="search-button">

<img class="search-icon" src="/Intro-to-html/youtube/search.svg">

<div class="tooltip">Search</div>

</button>

<button class="voice-search">

<img class="voice-icon" src="/Intro-to-html/youtube/voice-search-icon.svg">

<div class="tooltip">Search with your voice</div>

</button>

</div>

<div class="right-section">

<div class="upload-icon-container">

<img class="upload-icon"

src="/Intro-to-html/youtube/upload.svg">

<div class="tooltip">create</div>

</div>

<div class="youtube-apps-container">

<img class="youtube-apps"

src="/Intro-to-html/youtube/youtube-apps.svg">

<div class="tooltip">YouTube Apps</div>

</div>

<div class="notification-icon-container">

<img class="notification-icon"

src="/Intro-to-html/youtube/notifications.svg">

<div class="tooltip">Notifications</div>

<div class="notifications-count">3</div>

</div>

<div class="header-profile-container">

<img class="header-profile"

src="/9g/anime-girls-big-boobs.jpg">

<div class="tooltip">Profile</div>

</div>

</div>

</div>

<div class="sidebar">

<div class="sidebar-link">

<img src="/Intro-to-html/youtube/home.svg">

<div>Home</div>

</div>

<div class="sidebar-link">

<img src="/Intro-to-html/youtube/explore.svg">

<div>Explore</div>

</div>

<div class="sidebar-link">

<img src="/Intro-to-html/youtube/subscriptions.svg">

<div>Subscriptions</div>

</div>

<div class="sidebar-link">

<img src="/Intro-to-html/youtube/originals.svg">

<div>Originals</div>

</div>

<div class="sidebar-link">

<img src="/Intro-to-html/youtube/youtube-music.svg">

<div>YouTube Music</div>

</div>

<div class="sidebar-link">

<img src="/Intro-to-html/youtube/library.svg">

<div>Library</div>

</div>

</div>

<div class="video-grid">

<div class="preview">

<div class="thumbnail-row">

<a href="https://www.youtube.com/watch?v=n2RNcPRtAiY"

target="_blank">

<img class="thumbnail"

src="/Intro-to-html/Thumbnails/thumbnail-1.webp">

</a>

<div class="video-time">

14:20

</div>

</div>

<div class="video-info-grid">

<div class="channel-pic">

<div class="profile-picture-container">

<a href="https://www.youtube.com/watch?v=n2RNcPRtAiY"

target="_blank">

<img class="profile-pic"

src="/Intro-to-html/Channel Pics/channel-1.jpeg">

</a>

<div class="channel-tooltip">

<img class="channel-tooltip-picture"

src="/Intro-to-html/Channel Pics/channel-1.jpeg">

<div>

<div class="channel-tooltip-name">

<p>Marques Brownlee</p>

</div>

<div class="channel-tooltip-subs">

<p>15M subscribers</p>

</div>

</div>

</div>

</div>

</a>

</div>

<div class="video-info">

<a href="https://www.youtube.com/watch?v=n2RNcPRtAiY" target="_blank" class="video-link">

<p class="video-title">

Talking Tech and AI with Google CEO Sundar Pichai!

</p>

</a>

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

<a href="https://www.youtube.com/watch?v=mP0RAo9SKZk" target="_blank">

<img class="thumbnail" src="/Intro-to-html/Thumbnails/thumbnail-2.webp">

</a>

<div class="video-time">

8:22

</div>

</div>

<div class="video-info-grid">

<div class="channel-pic">

<a href="https://www.youtube.com/watch?v=mP0RAo9SKZk" target="_blank">

<img class="profile-pic" src="/Intro-to-html/Channel Pics/channel-2.jpeg">

</a>

</div>

<div class="video-info">

<a href="https://www.youtube.com/watch?v=mP0RAo9SKZk" target="_blank" class="video-link">

<p class="video-title">

Try Not To Laugh Challenge #9

</p>

</a>

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

<a href="https://www.youtube.com/watch?v=FgjPQQeTh1w" target="_blank">

<img class="thumbnail" src="/Intro-to-html/Thumbnails/thumbnail-3.webp">

</a>

<div class="video-time">

9:13

</div>

</div>

<div class="video-info-grid">

<div class="channel-pic">

<a href="https://www.youtube.com/watch?v=FgjPQQeTh1w" target="_blank">

<img class="profile-pic" src="/Intro-to-html/Channel Pics/channel-3.jpeg">

</a>

</div>

<div class="video-info">

<a class="video-link" href="https://www.youtube.com/watch?v=FgjPQQeTh1w">

<p class="video-title">

Crazy Tik Toks Taken Moments Before DISASTER

</p>

</a>

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

<a href="https://www.youtube.com/watch?v=094y1Z2wpJg" target="_blank">

<img class="thumbnail" src="/Intro-to-html/Thumbnails/thumbnail-4.webp">

</a>

<div class="video-time">

22:09

</div>

</div>

<div class="video-info-grid">

<div class="channel-pic">

<a href="https://www.youtube.com/watch?v=094y1Z2wpJg" target="_blank">

<img class="profile-pic" src="/Intro-to-html/Channel Pics/channel-4.jpeg">

</a>

</div>

<div class="video-info">

<a class="video-link" href="https://www.youtube.com/watch?v=094y1Z2wpJg">

<p class="video-title">

The Simplest Math Problem No One Can Solve - Collatz Conjecture

</p>

</a>

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

<a href="https://www.youtube.com/watch?v=86CQq3pKSUw" target="_blank">

<img class="thumbnail" src="/Intro-to-html/Thumbnails/thumbnail-5.webp">

</a>

<div class="video-time">

11:17

</div>

</div>

<div class="video-info-grid">

<div class="channel-pic">

<a href="https://www.youtube.com/watch?v=86CQq3pKSUw" target="_blank">

<img class="profile-pic" src="/Intro-to-html/Channel Pics/channel-5.jpeg">

</a>

</div>

<div class="video-info">

<a class="video-link" href="https://www.youtube.com/watch?v=86CQq3pKSUw">

<p class="video-title">

Kadane's Algorithm to Maximum Sum Subarray Problem

</p>

</a>

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

<a href="https://www.youtube.com/watch?v=yXWw0_UfSFg" target="_blank">

<img class="thumbnail" src="/Intro-to-html/Thumbnails/thumbnail-6.webp">

</a>

<div class="video-time">

19:59

</div>

</div>

<div class="video-info-grid">

<div class="channel-pic">

<a href="https://www.youtube.com/watch?v=yXWw0_UfSFg" target="_blank">

<img class="profile-pic" src="/Intro-to-html/Channel Pics/channel-6.jpeg">

</a>

</div>

<div class="video-info">

<a class="video-link" href="https://www.youtube.com/watch?v=yXWw0_UfSFg">

<p class="video-title">

Anything You Can Fit In The Circle I&#39;ll Pay For

</p>

</a>

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

## CSS -
```
p{

font-family: roboto, arial;

margin-top: 0;

margin-bottom: 0;

}

.thumbnail{

width: 100%;

}

.profile-pic{

width: 36px;

border-radius: 50px;

}

.video-title{

font-size: 14px;

font-weight: 500;

margin-top: 0;

line-height: 20px;

margin-bottom: 10px;

margin-left: 0;

margin-right: 0;

}

.video-link{

color: black;

text-decoration: none;

}

.thumbnail-row{

margin-bottom: 8px;

position: relative;

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

@media (max-width: 750px){

.video-grid{

grid-template-columns: 1fr 1fr;

}

}

@media (min-width: 751px) and (max-width: 999px){

.video-grid{

grid-template-columns: 1fr 1fr 1fr;

}

}

@media (min-width: 1000px){

.video-grid{

grid-template-columns: 1fr 1fr 1fr 1fr;

}

}

.video-time{

position: absolute;

background-color: black;

color: white;

bottom: 8px;

right: 5px;

font-family: roboto,arial;

font-weight: 500;

font-size: 12px;

padding-left: 4px;

padding-right: 4px;

padding-top: 4px;

padding-bottom: 4px;

border-radius: 2px;

}

.channel-tooltip{

background-color: white;

width: 200px;

padding: 12px 12px;

box-shadow: 2px 3px 10px rgba(0,0,0,0.3);

border-radius: 6px;

position: absolute;

top: 55px;

z-index: 300;

  

opacity: 0;

pointer-events: none;

  

display: flex;

align-items: center;

transition: opacity 0.15s;

}

.hover-tooltip-picture{

width: 50px;

height: 50px;

border-radius: 50px;

display: inline-block;

}

.profile-picture-container{

position: relative;

display: inline-block;

}

.profile-picture-container:hover .channel-tooltip{

opacity: 1;

}

.channel-tooltip-picture{

width: 50px;

height: 50px;

border-radius: 50px;

margin-right: 8px;

}

.channel-tooltip-name{

font-family: roboto,arial;

font-weight: bold;

font-size: 16px;

margin-bottom: 4px;

}

.channel-tooltip-subs{

font-family: roboto,arial;

color: rgb(96,96,96);

font-size: 14px;

}
```

## CSS Shorthand Properties
### Padding shorthand -
You can use <mark style="background: #FF5582A6;">padding: 4px 10px</mark> instead of -
* padding-left: 4px;
* padding-right:4px;
* padding-top:10px;
* padding-bottom:10px;

The first value is vertical padding, while then second is horizontal padding. But, if you add 4 values to it, It acts top, right, bottom, and left -
<mark style="background: #FF5582A6;">padding: 4px 10px 4px 10px;</mark>

You can remember it easily as it works clockwise. <mark style="background: #FFB86CA6;">The same can be applied to margins</mark>.

### Border Shorthand properties -
You can use shorthand for borders as well -
* border-width: 1px;
* border-style: solid;
* border-color: rgb(192,192,192);

You can use -
<mark style="background: #FF5582A6;">border: 1px solid rgb(192,192,192);</mark>

### Inheritance -
If you use an element for the main property, the values are passed down to the properties under it as well -
video-gird{
text-decoration: underline;
}

Which makes everything in it underlined.
![Screenshot_1 33.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%2033.png)

This does not apply to all the properties, though. It can only apply to the text properties and is passed down from the outer elements to the inner elements.

## Semantic Elements -
These work the same way as DIV elements, but have a special meaning to the screen readers, search engines or other devices or robots.
These are -
```
<header></header>
<nav></nav>
<main></main>
<section></section>
```

## Comments -
Comments are something that is ignored by the search engines, robots, etc. but can be read by us in the code. We can write comments in HTML by -
```
<!--comment-->
```

We can write comments in CSS by -
```
/* Comment */
```

Comments are extra information you can add to a code without effecting our webpage. This can be really important if you're working with a team or have to remember something for later.