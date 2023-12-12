---
{"dg-publish":true,"permalink":"/html-and-css/chapter-8-css-display-property/","noteIcon":"1"}
---

🧶 Tags - #HTML_CSS 

---
Resources - [[]]
 
---
Links - https://github.com/SuperSimpleDev/html-css-course-2022/tree/main/1-exercise-solutions/lesson-08
 
 ---
# Display Properties in CSS
In HTML there are 3 types of elements
1. <mark style="background: #D2B3FFA6;">Block element</mark>
		A block element takes up the entire line. So, for example, a <mark style="background: #FFB86CA6;">paragraph</mark> by default is a block element. So regardless of what width you set for the line, they take up the entire line.
2. <mark style="background: #CACFD9A6;">Inline-block element</mark>
		An inline-block elements takes up just as much space as it needs to. Example of an inline-block elements are <mark style="background: #FFB86CA6;">image</mark> and <mark style="background: #FFB86CA6;">input</mark> elements.
3. <mark style="background: #FFB8EBA6;">Inline element</mark>
		Inline elements are just text elements, they appear within a line of text. An example of line element is <mark style="background: #FFB86CA6;">strong</mark> element.

Between these 3 elements, the block and inline-block elements are the most interesting, because they determine how these elements are displayed on the page.

In addition to this, we can use a CSS property called <mark style="background: #FF5582A6;">display</mark> to switch between block and inline-block

We can target multiple classes to together in CSS with this syntax, as it takes less space.
```
.author,
.stats{
display: inline-block;
}
```

# Exercise 8a-8c -
![Screenshot_1 8.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%208.png)

# HTML
```
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link rel="stylesheet" href="displayblock.css">

<title>Display Block Practice</title>

</head>

<body>

<input class="t" type="text" placeholder="Name">

<input class="t" type="text" placeholder="Email">

<p class="chat">Thanks for chatting with our

customer support. Would you like to take

our quick survey?

</p>

<button class="yn">Yes</button>

<button class="yn">No</button>

<br>

<img class="logo" src="purepng.com-google-logo-2015brandlogobrand-logoiconssymbolslogosgoogle-6815229372333mqrr.png">

<input class="search" type="text" placeholder="Search Google or type a URL">

</body>

</html>
```

# CSS
```
.t{

display: block;

margin: 5px;

}

.chat{

width: 220px;

display: inline-block;

vertical-align: middle;

}

.yn{

vertical-align: middle;

}

.logo{

display: block;

margin-left: 110px;

width: 150px;

margin-bottom: 10px;

}

.search{

font-size: 15px;

display: block;

padding-left: 10px;

padding-right: 100px;

padding-top: 6px;

padding-bottom: 6px;

border: none;

border-radius: 50px;

width: 250px;

box-shadow: 0 1px 5px rgb(122, 122, 122);

}
```

# Exercise 8d-8e -

![Screenshot_1 9.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%209.png)

# HTML

```
<!doctype html>

<html>

<head>

<title>Display Exercises</title>

<link rel="stylesheet" href="exercise8d8e.css">

</head>

<body>

<input class="first" type="text" placeholder="First name">

<input class="first" type="text" placeholder="Last name">

<input class="email" type="text" placeholder="Email">

<button class="signup">Sign Up</button>

  

<p class="heading">Request a ride now</p>

<input class="e" type="text" placeholder="Enter pickup location">

<input class="e" type="text" placeholder="Enter destination">

<button class="b">Request now</button>

<button class="s">Schedule for later</button>

</body>

</html>
```

# CSS

```
.first{

width: 120px;

margin-top: 5px;

padding-top: 10px;

padding-bottom: 10px;

display: inline-block;

border-radius: 5px;

border-width: 1px;

}

.email{

display: block;

margin-top: 12px;

width: 250px;

padding-top: 10px;

padding-bottom: 10px;

border-radius: 5px;

border-width: 1px;

margin-bottom: 12px;

}

.signup{

display: block;

margin-top: 12px;

width: 255px;

padding-top: 10px;

padding-bottom: 10px;

border-radius: 6px;

border: none;

margin-bottom: 12px;

font-size: 15px;

color: white;

background-color: rgb(0, 89, 255);

}

  

.heading{

font-size: 28px;

font-weight: 400;

}

.e{

display: block;

width: 270px;

padding-top: 10px;

padding-bottom: 10px;

background-color: rgb(233, 233, 233);

margin-top: 5px;

padding-left: 10px;

border: none;

color: black;

}

.b{

margin-top: 20px;

padding-top: 10px;

padding-bottom: 10px;

padding-left: 15px;

padding-right: 15px;

margin-right: 5px;

background-color: black;

color: white;

border: none;

border-radius: 2px;

}

.s{

margin-top: 20px;

padding-top: 10px;

padding-bottom: 10px;

padding-left: 15px;

padding-right: 15px;

margin-right: 5px;

background-color: rgb(233, 233, 233);

color: black;

border: none;

border-radius: 2px;

}
```