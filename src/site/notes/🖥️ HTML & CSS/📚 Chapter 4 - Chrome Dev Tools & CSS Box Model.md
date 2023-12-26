---
{"banner":"![florian-olivo-4hbJ-eymZ1o-unsplash.jpg](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/florian-olivo-4hbJ-eymZ1o-unsplash.jpg)","dg-publish":true,"permalink":"/html-and-css/chapter-4-chrome-dev-tools-and-css-box-model/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-11-14T21:08:36.646+05:30","updated":"2023-12-12T07:35:40.904+05:30"}
---

 🧶 Tags - #HTML_CSS 

---
 Resources - [[]]

---
 Links - https://github.com/SuperSimpleDev/html-css-course-2022/tree/main/1-exercise-solutions/lesson-04
 
# [[🖥️ HTML & CSS/📚 Chapter 4 - Chrome Dev Tools & CSS Box Model\|📚 Chapter 4 - Chrome Dev Tools & CSS Box Model]]
==2022-11-02 - 20:05==

---
#  How to use Dev tools to see the data of the webpage
![Pasted image 20221102201513.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Pasted%20image%2020221102201513.png)
Like you can get the perfect color that you see on the web page by looking at the styling code provided in dev tools.
You can see all kinds of styling and other attributes used in the page.

# CSS Box Model
* Margins - margins are on the outside of the elements.
<mark style="background: #ADCCFFA6;">.button{
margin-top: 10px;
}</mark>
* Padding - works on the inside of the elements.
<mark style="background: #ADCCFFA6;">.button{
padding-top: 10px
}</mark>

### We can also use - Vertical-align: top; - to align item that are not aligned due to padding and size issues

### These properties determine how much space an element takes on a page.

You can see the box model in the dev tools to see the size, width, margin, padding, etc of the elements.
![Screenshot_1 1.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%201.png)
---
# Exercise 4a-4e
Use 3a-3e with padding instead of height/width.

```
<style>

.requestnow{

background-color: black;

color: white;

padding-top: 12px;

padding-bottom: 12px;

padding-left: 16px;

padding-right: 16px;

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

padding-left: 42px;

padding-top: 12px;

padding-bottom: 12px;

padding-right: 42px;

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

padding-top: 12px;

padding-bottom: 12px;

padding-left: 20px;

padding-right: 20px;

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

padding-top: 12px;

padding-bottom: 12px;

padding-left: 18px;

padding-right: 18px;

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

padding-top: 12px;

padding-bottom: 12px;

padding-left: 18px;

padding-right: 18px;

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

padding-top: 12px;

padding-bottom: 12px;

padding-left: 26px;

padding-right: 26px;

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

padding-top: 12px;

padding-bottom: 12px;

padding-left: 22px;

padding-right: 22px;

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
---
# Exercise 4f - Update the tweet button in buttons.html by using padding instead of height/width

# Exercise 4g - Use dev Tools to get the exact color of the subscribe button and update in the code
### I've updated it with the latest colors which are white and black(with opacity)

![Screenshot_1 7.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%207.png)

```
<style>

*{

background-color: pink;

}

.subscribe-button{

background-color: fff;

color: black;

border: none;

height: 36px;

width: 105px;

border-radius: 2px;

cursor: pointer;

margin-right: 8px;

transition: opacity 0.15s;

}

  

.subscribe-button:hover{

opacity: 0.8;

}

.subscribe-button:active{

background-color: black;

color: white;

opacity: 0.9;

}

.join{

background-color: white;

color: rgb(0, 204, 255);

border-color: rgb(0, 204, 255);

border-style: solid;

border-width: 1px;

height: 36px;

width: 62px;

border-radius: 2px;

cursor: pointer;

margin-right: 8px;

transition: background-color 0.15s,

color 0.15s;

}

.join:hover{

background-color: rgb(0, 204, 255);

color: white;

}

.join:active{

opacity: 0.7;

}

.tweet{

background-color: rgb(0, 110, 255);

color: white;

border: none;

padding-top: 9px;

padding-bottom: 9px;

padding-left: 14px;

padding-right: 14px;

border-radius: 50px;

cursor: pointer;

font-weight: bold;

font-size: 15px;

transition: box-shadow 0.15s;

}

.tweet:hover{

box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.15);

}

</style>

<button class="subscribe-button">

SUBSCRIBE

</button>

<button class="join">

JOIN

</button>

<button class="Tweet">

Tweet

</button>
```

# Exercise 4h-4k -

![Screenshot_1 2.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%202.png)

```
<style>

.back{

margin-left: 10px;

margin-right: 10px;

padding-top: 10px;

padding-bottom: 10px;

padding-left: 10px;

padding-right: 10px;

cursor: pointer;

}

.next{

margin-left: 10px;

margin-right: 10px;

padding-top: 10px;

padding-bottom: 10px;

padding-left: 10px;

padding-right: 10px;

cursor: pointer;

}

.result{

margin-left: 4px;

margin-right: 4px;

cursor: pointer;

}

.stretch{

background-color: green;

padding-right: 12px;

padding-left: 12px;

padding-top: 8px;

padding-bottom: 8px;

border: none;

color: white;

font-weight: 600;

transition: 1s;

vertical-align: top;

cursor: pointer;

}

.stretch:hover{

padding-right: 22px;

padding-left: 22px;

padding-top: 16px;

padding-bottom: 16px;

}

.d{

background-color: green;

padding-right: 12px;

padding-left: 12px;

padding-top: 8px;

padding-bottom: 8px;

border: none;

color: white;

font-weight: 600;

vertical-align: top;

box-shadow: 5px 5px 5px rgba(0,0,0,0.15);

cursor: pointer;

}

.d:active{

margin-right: 0px;

margin-left: 2px;

margin-top: 2px;

margin-bottom: 0px;

box-shadow: 0 0 0 rgba(0,0,0,0);

}

.three{

background-color: green;

padding-right: 12px;

padding-left: 12px;

padding-top: 8px;

padding-bottom: 8px;

border: none;

color: white;

font-weight: 600;

vertical-align: top;

cursor: pointer;

transition: padding 0.15s,

margin 0.15s;

margin-top: 10px;

margin-left: 10px;

margin-right: 10px;

}

.three:hover{

padding-right: 25px;

padding-left: 25px;

margin-left: 0px;

margin-right: 0px;

}

</style>

<button class="Back">Back</button>

<a class="result" href="">1</a>

<a class="result" href="">2</a>

<a class="result" href="">3</a>

<a class="result" href="">4</a>

<a class="result" href="">5</a>

<button class="next">Next</button>

<button class="stretch">Stretch</button>

<button class="d">Shadow</button>

<br>

<button class="three">One</button>

<button class="three">Two</button>

<button class="three">Three</button>
```