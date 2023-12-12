---
{"dg-publish":true,"permalink":"/html-and-css/chapter-3-hovers-transitions-shadows/","noteIcon":"1"}
---

 🧶 Tags - #HTML_CSS 

---
 Resources - [[]]
 
---
 Links - https://github.com/SuperSimpleDev/html-css-course-2022/tree/main/1-exercise-solutions/lesson-03
 
# [[🖥️ HTML & CSS/📚 Chapter 3 - Hovers, Transitions, Shadows\|📚 Chapter 3 - Hovers, Transitions, Shadows]]
==2022-11-02 - 13:55==

![Pasted image 20221102141325.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Pasted%20image%2020221102141325.png)
# Exercise 3-1 - Different Button Style For Hover, Transition, Shadows

```
<style>

.requestnow{

background-color: black;

color: white;

height: 40px;

width: 110px;

border: none;

margin-left: 5px;

margin-right: 5px;

border-radius: 2px;

cursor: pointer;

transition: opacity 0.15s;

}

.requestnow:hover{

opacity: 0.8;

}

.addtocart{

background-color: rgb(255,216,20);

color: black;

height: 40px;

width: 150px;

border: none;

border-radius: 50px;

margin-left: 5px;

margin-right: 5px;

cursor: pointer;

transition: background-color 0.15s;

}

.addtocart:hover{

background-color: rgb(226, 194, 35);

}

.signup{

background-color: rgb(46,164,79);

color: white;

height: 40px;

width: 95px;

border: none;

border-radius: 8px;

margin-left: 5px;

margin-right: 5px;

font-weight: bold;

font-size: 16px;

cursor: pointer;

transition: box-shadow 0.15s;

}

.signup:hover{

box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.15);

}

.getstarted{

background-color: rgb(121,82,179);

color: white;

height: 40px;

width: 110px;

border: none;

border-radius: 4px;

margin-left: 5px;

margin-right: 5px;

font-weight: bold;

font-size: 14px;

cursor: pointer;

transition: background-color 0.15s;

}

.getstarted:hover{

background-color: rgb(103, 68, 155);

}

.download{

background-color: white;

color: rgb(108,117,125);

height: 40px;

width: 110px;

border-style: solid;

border-color: rgb(108,117,125);

border-radius: 4px;

margin-left: 5px;

margin-right: 5px;

font-weight: bold;

font-size: 14px;

cursor: pointer;

transition: 0.15s;

}

.download:hover{

background-color: rgb(108,117,125);

color: white;

}

.aocw{

background-color: rgb(10,102,194);

color: white;

height: 40px;

width: 250px;

border: none;

border-radius: 50px;

margin-left: 5px;

margin-right: 5px;

font-weight: bold;

font-size: 16px;

cursor: pointer;

transition: 0.15s;

}

.aocw:hover{

background-color: rgb(11, 79, 146);

}

.save{

background-color: white;

color: rgb(10,102,194);

height: 40px;

width: 80px;

border-width: 1px;

border-style: solid;

border-color: rgb(10,102,194);

border-radius: 50px;

margin-left: 5px;

margin-right: 5px;

font-weight: bold;

font-size: 16px;

margin-top: 10px;

cursor: pointer;

}

.save:hover{

background-color: rgb(174, 214, 255);

border-width: 2px;

}

</style>

  

<button class="requestnow">

Request Now

</button>

<button class="addtocart">

Add to Cart

</button>

<button class="signup">

Sign up

</button>

<button class="getstarted">

Get started

</button>

<button class="download">

download

</button>

<button class="aocw">

Apply on company website

</button>

<button class="save">

Save

</button>
```

# Exercise 3f - Color Change on Click

```
<style>

h1{

font-weight: 800;

}

a{

color: rgb(0, 113, 133);

transition: color 1s;

}

a:hover{

color: rgb(175, 50, 50);

}

h3{

color: rgb(0,118,0);

}

.atc{

background-color: rgb(255,216,20);

color: black;

width: 150px;

height: 40px;

font-size: 18px;

border: none;

border-radius: 50px;

cursor: pointer;

margin-right: 7px;

}

.atc:active{

opacity: 0.5;

}

.Buynow{

background-color: rgb(255,164,28);

color: black;

width: 150px;

height: 40px;

font-size: 18px;

border: none;

border-radius: 50px;

cursor: pointer;

}

.Buynow:active{

opacity: 0.5;

}

</style>

<a href="">Back to Amazon</a>

<h1>Nike Black Running Shoes</h1>

<h3>$39 - in stock.</h3>

<h4>Free delivery tomorrow.</h4>

<button class="atc">Add to Cart</button>

<Button class="Buynow">Buy now</Button>
```

---
