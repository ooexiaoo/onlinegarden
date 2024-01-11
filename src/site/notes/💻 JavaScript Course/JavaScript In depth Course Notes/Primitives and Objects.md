---
{"banner":"![ivan-boyko-clouds-morning.gif](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/ivan-boyko-clouds-morning.gif)","banner_icon":"🖥️","dg-publish":true,"permalink":"/java-script-course/java-script-in-depth-course-notes/primitives-and-objects/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-11-14T21:08:36.569+05:30","updated":"2024-01-11T03:46:17.265+05:30"}
---

🧶 Tags:: #JavaScript 
🗃 Resources:: [YouTube](https://www.youtube.com/watch?v=qpU3WIqRz9I&list=PLu0W_9lII9ahR1blWXxgSlL4y9iQBnLpR&index=4) | [Replit](https://replit.com/@ooexiaoo/04PrimitivesObjects#index.js)
==2023-09-04 - 02:35==

## There are 7 types of data types -
**NNBBSSU**

NULL
NUMBER
SYMBOL
STRING
BOOLEAN
BIGINT
UNDEFINED

```JavaScript
// NN BB SS U
let a = null;
let b = 2;
let c = true;
let d = BigInt("567") + BigInt("3");
let e = "EXIA";
let f = Symbol("I'm nice");
let g = undefined
console.log(a, b, c, d, e, f, g)
console.log(typeof e) // string

// Objects on JS
const item = {
  "varun": true,
  "Josh": 55,
  "Pushkar": undefined
}
console.log(item["varun"]); // true

// create a data type string and try to add a number to it
let example = "master";
let h = example + 30;
console.log(typeof h) // string

const items = {
  "varuni": true,
}

let varuni = 3;
console.log(varuni) // 3

const dictionary = {
  "apple": "a fruit",
  "wheat": "a type of grain",
  "car": "A type of vehicle",
  "bike": "A type of vehicle!",
  "earth": "The planet we live on",
}

console.log(dictionary.apple) // a fruit
console.log(dictionary.wheat) // a type of grain
console.log(dictionary.car) // a type of vehicle
console.log(dictionary.bike) // a type of vehicle
console.log(dictionary.earth) // The planet we live on

// chapter 1 - Q1
let x = "varun"
let y = 6
console.log(x + y) // when you add 2 things in a string format they concatenate

// Chapter 1 - Q2
console.log(typeof (x+y))

// chapter 1 - Q3
const t = {
  name: "varun",
  section: 1,
  isPrincipal: false
}

t['code name'] = 'exia'  // adding key value to an const, you can add and change keys inside an object
t['name'] = "varun2"  // changing key value { name: 'varun2', section: 1, isPrincipal: false, 'code name': 'exia' }
console.log(t)
```