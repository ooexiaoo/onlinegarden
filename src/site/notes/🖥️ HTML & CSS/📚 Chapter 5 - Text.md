---
{"banner":"![florian-olivo-4hbJ-eymZ1o-unsplash.jpg](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/florian-olivo-4hbJ-eymZ1o-unsplash.jpg)","dg-publish":true,"permalink":"/html-and-css/chapter-5-text/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-11-14T21:08:36.598+05:30","updated":"2023-12-12T07:35:46.255+05:30"}
---

 🧶 Tags - #HTML_CSS 

---
 Resources - [[]]
 
---
 Links -
 
# [[🖥️ HTML & CSS/📚 Chapter 5 - Text\|📚 Chapter 5 - Text]]
==2022-11-03 - 12:57==

---
###  CSS Entity
As we can't add check mark or dots in HTML we need a code called **HTML entity**
Example - for check mark we can use <mark style="background: #FF5582A6;">'&#10003;'</mark>

### CSS Specificity
CSS Classes work on a hierarchy, so a browser will follow this hierarchy when showing the page.
Example - p{
margin-top: 10px;
}
.text{
margin-top:20px;
}
**p class="text">This is a test**

In this scenario <mark style="background: #FF5582A6;">.text</mark> will be given the priority because it's not a general <mark style="background: #FF5582A6;">"p"</mark> tag but, a specific tag for a particular element

### Text Element
A text element is an element that's inside a line of text
Example - strong, u, span, etc.

Span is the most generic element. You can add class elements to any of these to style them further.

![Pasted image 20221103165402.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Pasted%20image%2020221103165402.png)

# Text Code Example -
![Screenshot_1 4.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%204.png)
```
<style>

p{font-family: Arial;

margin-top: 0;

margin-bottom: 0;

}

.videotitle{

font-family: arial;

font-weight: bold;

font-size: 18px;

width: 280px;

line-height: 24px;

margin-bottom: 5px;

}

.stats{

font-size: 14px;

color: rgb(96, 96, 96);

margin-top: 0px;

}

.mkbhd{

font-weight: 400;

font-size: 14px;

color: rgb(96, 96, 96);

margin-top: 20px;

margin-bottom: 20px;

}

.talk{

font-size: 14px;

color: black;

margin-top: 0px;

width: 280px;

line-height: 22px;

margin-top: 0%;

margin-bottom: 100px;

}

.apple{

margin-bottom: 50px;

font-size: 14px;

background-color: #e34140;

color: white;

text-align: center;

padding-top: 18px;

padding-bottom: 18px;

}

.span-example{

cursor: pointer;

}

.span-example:hover{

text-decoration: underline;

}

</style>

  

<p class="videotitle">

Talking Text and AI with Google CEO Sundar Pichai!

</p>

<p class="stats">

3.4m Views &#183; 6 months ago

</p>

<p class="mkbhd">Marques Brownlee &#10003;</p>

<p class="talk">Talking tech and AI on the heels of Google I/O,

Also a daily driver phone reveal from Google's CEO. Shoutout to Sundar!</p>

<p class="apple">Shop early for the best selection of holiday favourites.

<span class="span-example">Shop now &gt;</span>

</p>
```

# Exercise 5a-5d



![Screenshot_1 3.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%203.png)
```
<style>

p{

line-height: 20px;

}

.tahoma{

font-family: Tahoma;

font-weight: bold;

}

.arial{

font-family: arial;

font-size: large;

font-weight: bold;

}

.italic{

font-style: italic;

font-weight: 400;

color: red;

}

.course{

font-family: verdana;

font-size: large;

font-weight: bold;

margin-bottom: 0;

}

.gray{

font-family: verdana;

color: gray;

margin-top: 0;

}

.learn{

font-family: verdana;

width: 260px;

}

button{

padding-left: 20px;

padding-right: 20px;

background-color: rgb(4, 128, 0);

color: white;

padding-top: 10px;

padding-bottom: 10px;

border: none;

border-radius: 10px;

}

.arial-one{

font-family: arial;

font-size: large;

font-weight: bold;

text-align: center;

}

.para{

font-family: arial;

text-align: center;

font-size: 14px;

}

.learn-more{

font-family: arial;

color: rgb(0, 183, 255);

text-align: center;

}

</style>

<p class="tahoma">This is Tahoma Font</p>

<p class="arial">Biggest Deal of the Year!<br>

<span class="italic">Sales end Tuesday</span>

</p>

<p class="course">HTML CSS Course</p>

<p class="gray">Beginner to Pro</p>

<p class="learn">In this course, we'll learn the skills

you need to become a developer.

</p>

<button>Get Started</button>

<p class="arial-one">Shopping for your business?</p>

<p class="para">See how Apple at Work can help.</p>

<p class="learn-more">Learn more &gt;</p>
```


# Exercise 5e-5g
![Screenshot_4.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_4.png)

```
<style>

p{

font-family: arial;

margin-top: 8px;

margin-bottom: 0;

text-align: center;

margin-left: 15px;

}

.new{

color: red;

text-align: center;

font-size: 12px;

font-weight: 700;

}

.mpro{

text-align: center;

font-size: 25px;

font-weight: bold;

}

.spro{

text-align: center;

font-size: 35px;

font-weight: 900;

}

.price{

text-align: center;

font-size: 16px;

font-weight: 300;

margin-bottom: 15px;

}

.buy{

background-color: rgb(0, 89, 255);

color: white;

text-align: center;

border-radius: 30px;

font-size: 12px;

border: none;

padding-top: 7px;

padding-bottom: 7px;

padding-left: 15px;

padding-right: 15px;

font-weight: bold;

cursor: pointer;

}

.num{

font-size: 40px;

text-align: left;

color: black;

padding-right: 5px;

}

.usd{

text-align: left;

color: gray;

}

.green{

text-align: left;

color: green;

}

.after{

text-align: left;

color: gray;

}

.red{

color: red;

}

.org{

margin-top: 20px;

text-align: left;

font-size: large;

font-weight: bold;

}

.at-1{

font-weight: 400;

color: rgb(90, 90, 90);

}

.para-1{

text-align: left;

width: 500px;

font-size: large;

font-weight: 400;

margin-bottom: 15px;

}

.para{

text-align: left;

font-size: 16px;

font-weight: 500;

}

.at{

color: rgb(0, 140, 255);

}

</style>

<p class="new">New</p>

<p class="mpro">MacBook Pro</p>

<p class="spro">Superchaged for pros.

</p>

<p class="price">From $1999</p>

<p><span class="buy">Buy</span></p>

  

<p class="usd"><span class="num">1,049.61</span> USD</p>

<P class="green">+18.05 (1.75%) today</P>

<p class="after">After hours 1,048.00<span class="red"> -1.61 (0.15%)</span></p>

  

<p class="org">freeCodeCamp.org <span class="at-1">@freeCodeCamp 1h</span></p>

<p class="para-1">As a web developer, you'll want to make your

projects easy to use and navigate around.</p>

<p class="para">Here <span class="at">@Chp_it</span> outlines the top skills

new developers should have.</p>

---
