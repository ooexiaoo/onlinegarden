---
{"banner":"![florian-olivo-4hbJ-eymZ1o-unsplash.jpg](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/florian-olivo-4hbJ-eymZ1o-unsplash.jpg)","dg-publish":true,"permalink":"/html-and-css/chapter-7-images-and-text-boxes/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-11-14T21:08:36.610+05:30","updated":"2023-12-12T19:57:05.346+05:30"}
---

 🧶 Tags - #HTML_CSS 

---
 Resources - [[]]
 
---
 Links - https://github.com/SuperSimpleDev/html-css-course-2022/tree/main/1-exercise-solutions/lesson-07
 
---
# Loading Images Into The Site
To load images onto the site, we'll use a void tag 'img'
```
<img src="thumnail.jpg" alt="thumbnail1">
```
You are free to not use alt tag if you need, but is recommended for showing image titles that you might have.

When we resize images, the images tend to maintain the same aspect ratio if given just one parameter, like only width or only height
```
width="300px"
```

Aside from height and width, we have specific properties we can use for 'img' elements and this is 'object-fit' property, which determines what happens to the image inside the given height and width parameters.
```
object-fit="cover"
```

We can also adjust which part of the image we see with 'object-postition', like object-position="left' will show the left part of the image. We can also use object-position="contain" which will shrink down the image with the correct aspect ratio fit inside the given height and width we have defined.
```
object-position="left"
or
object-postition="contain"
```

# Search Box
To create a search box, we use a void element called 'input'
```
<input type="text">
```

Another type we can use is a 'checkbox'
```
<input type="checkbox">
```

You can also add a placeholder attribute to the search box to show what kind of input you desire from your users, like search...
The placeholder also disappears  as we start typing. 
```
<input type="text" placeholder="search">
```

You can also add a class element to use all the CSS properties
```
<input class="search-bar" type="text" placeholder="search">
```

Then you can use CSS to modify the search box as desired
```
.search-bar{

font-size: 20px;

margin-left: 12px;

}
```

# Exercise 7a-7g -

![Screenshot_1 6.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%206.png)

# HTML
```
<!DOCTYPE html>

<html>

<head>

<title>Exercise 7</title>

<link rel="stylesheet" href="style.css">

</head>

<body>

<img class="imga" src="images/wp5208206-cute-anime-girl-hd-wallpapers.jpg">

<img class="imgb" src="images/wp5208206-cute-anime-girl-hd-wallpapers.jpg">

<img class="imgc" src="images/wp5208206-cute-anime-girl-hd-wallpapers.jpg">

  

<input class="simple-search" type="text" placeholder="Search">

<input class="googlesearchbox" type="text"

placeholder="Search Google or type a URL">

  

<p class="email">Email</p>

<input class="email1" type="text">

<P class="terms">By clicking Agree & Join, you agree to the Privacy Policy.</P>

<button class="join">Agree & Join</button>

<br>

<img class="logo" src="images/wp5208206-cute-anime-girl-hd-wallpapers.jpg">

<input class="tweet" type="text" placeholder="What's happening?">

<button class="tweet-button">Tweet</button>

</body>

</html>
```

# CSS

```
*{

margin: 20px;

}

.imga{

width: 200px;

border-radius: 10px;

}

.imgb{

width: 200px;

height: 200px;

object-fit: cover;

}

.imgc{

width: 200px;

height: 200px;

object-fit: cover;

border-radius: 50%;

}

.simple-search{

padding-top: 5px;

padding-bottom: 5px;

border-style: groove;

border-radius: 5px;

}

.googlesearchbox{

width: 500px;

padding-top: 12px;

padding-bottom: 12px;

padding-left: 15px;

padding-right: 15px;

border-radius: 20px;

border: none;

box-shadow: 0 1px 5px rgb(122, 122, 122);

margin-top: 20px;

margin-left: 20px;

}

.email{

font-size: 15px;

color: rgb(78, 78, 78);

margin-bottom: 0;

}

.email1{

width: 400px;

padding-top: 10px;

padding-bottom: 10px;

border-radius: 3px;

margin-bottom: 8px;

margin-top: 8px;

}

.terms{

margin-top: 10px;

font-size: 15px;

width: 400px;

align-items: center;

}

.join{

width: 400px;

padding-left: 40px;

padding-right: 40px;

background-color: rgb(0, 102, 255);

color: white;

padding-top: 10px;

padding-bottom: 10px;

font-size: 20px;

border-radius: 50px;

margin-top: 0px;

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
```