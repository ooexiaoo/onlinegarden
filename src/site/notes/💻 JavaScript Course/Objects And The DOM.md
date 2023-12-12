---
{"dg-publish":true,"permalink":"/java-script-course/objects-and-the-dom/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-11-14T21:08:36.552+05:30","updated":"2023-12-12T07:34:49.424+05:30"}
---

🧶 Tags - #JavaScript 

---
🗃Resources - [[]]

---
🔗Links - https://app.pluralsight.com/course-player?clipId=459ca21f-01aa-4b88-8d44-f37341f4069c

# [[💻 JavaScript Course/Objects And The DOM\|Objects And The DOM]]
==2023-01-03 - 18:44==

---
We've already seen how objects can contain multiple values or properties that are related. What a DOM stands for is a **Document Object Model**. When we wanna work with a web page in JavaScript, the key object we work with is **document** and the DOM refers to that document object, along with all it's supporting objects and other features.

## Object Properties
Objects usually have several properties. You can think of an object as a group of values or properties.

### Simple Object Properties
```
let person = {
	name: "John",
	age: 32,
	partTime: false
};

console.log(person.name);   // John - property name

console.log(person.age);    // 32

console.log(person.partTime);  // false
```

When you're working with objects, make sure that you're working with properties that exist.

### Changing Object Properties
```
let person = {
	name: "John",
	age: 32,
	partTime: false
};

person.age = 33;

showMessage(person.age);   // 33
```

Here we're using a **'.'** syntax to access an object property, but you can also use square brackets - **['age']**, the property name needs to be a string. **Age** as a string.

### Using Advanced Data Type - Symbol
```
let mySymbol = symbol();   // created a new symbol

let person = {
	name: "John",
	age: 32,
	partTime: false,
	[mySymbol]: 'secretInformation'  // no need to use '' as this is a variable name
};

person.age = 33;

showMessage(person.age);   // 33
```

With symbols, we can access some custom information that only we can get access to. This is an advanced scenario. For example, you could be working with an HR system that wanted to hide salary information, or some kind of plugin architecture, where each plugin had its own secret information specific to that plugin.

We won't be using this much, but it's useful because the only one who had access to the code **mySymbol** would be able to access **'secretInformation'**.

## Object Methods
We've seen how the objects can be composed of data, those are the object's properties, but we can also attach functions directly to objects. And those functions are called methods.

### Adding Method
```
let person = {
	name: "John",
	age: 32,
	partTime: false,
	showInfo: function(realAge) {
		showMessage(this.name + ' is ' + realAge);
	}
};

person.showInfo(34);  // John is 34
```

If we just use the word **name** in **showMessage** the code doesn't execute properly as it doesn't know which name?! To rectify that, we use **this** keyword because **this** refers to the current object.

We would call **showInfo** a method because it's part of an object, but some developers still refer to this as a function, which is also true. But because it's attached to an object, it's traditionally called a method.

## Passing Objects To Functions
There is a big difference between passing an object to a function Vs passing a built-in type such as a string, a number, or a boolean value. **This is a source of a lot of problems and bugs**.

### Passing Strings To Functions Example
```
let message = 'Hello';

function changeMessage(message) {
	message = 'Hi!';
}

changeMessage(message);

showMessage(message);   // Hello
```

* When we call **changeMessage(message);** it actually took the value of **'Hello'** store it in the parameter **function changeMessage(message)**
* and in function **message = 'Hi!'** only changed the parameter **function changeMessage(message)** it didn't change our original **message**.
* So by the time we call **showMessage(message)** we're still working with our original **message = 'Hello'** variable.

This is not how objects work. So we'll take a look into that now.

### Passing Objects To Functions Example
```
let person = {
	name: 'John',
	age: 32,
	partTime: false
};

function incrementAge(person) {
	person.age++;
}

incrementAge( person );

showMessage(person.age);  // 33
```

Because we're passing an object to increment age when we access properties or methods on that object, we are able to change them.

We can't change **person** itself as an object, but we access all of its properties, sub properties and methods. This is called passing by reference.

It's important to do a lot of practice sending values to functions and practice sending objects to functions

## Standard Built-in Objects
#### Ref Link - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects

### Converting Dates To Strings
```
let now = new Date();
showMessage( now.toDateString() );  // You will get current date
```

We can use this to call a lot of different variables. As shown on Mozilla Developers Page.

### Math To Absolute Value
```
showMessage( Math.abs(-42) );  // 42
showMessage( Math.random() );  // You'll get a decimal number
```

### Character At A Specific Index In A String
```
let s = 'Hello';
showMessage( s.charAt(0));  // H
```

## The Document Object Model (DOM)
Popular use of JavaScript has been as a scripting language behind web-pages, but we can also use JavaScript now with technologies like **node.js** to run JavaScript on servers. And with Cordova we can run JavaScript apps on mobile devices/tablets.

In this one, we'll focus mostly on web browser programming. And we've already been using the DOM in our exercises.

### DOM Example
```
function showMessage(message) {
	document.getElementbyId('message').textcontent = message;
}
```

* **Document** represents the web-page.
* **.getElementById** is the method.
* This DOM returns another DOM object which has a property **.textContent** which is the text that we see on the web-page.

We can refer to MDN documentation for more.

## Styling DOM Elements
Normally we would style a file using CSS file or pre-processor technology such as ECSS or SCSS. But occasionally we want to control it with JavaScript.

### Styling With JavaScript Example
```
const header = document.getElementById('message');

header.style.color = 'red';
header.style.fontWeight = '100';
```

Many times, CSS properties have a **"-"** in them, like **font-weight**. The problem is, we can't use a **"-"** in JavaScript. So instead we use camelCase. So we use **fontWeight**.

## Detecting Button Clicks
In JavaScript there are often times when we want to know if the user has interacted with the web-page and the simplest interaction is by clicking a button.

### Click Detection Example
```
const button = document.getElementById('see-review');

button.AddEventListener('click', function() {
	console.log('click');
});
```

## Showing And Hiding DOM Elements
We can show and hide particular sections on click. In the example below, we'll show and hide the review section on click detection.

### The DIV We Added
```
<div id="review" class="container d-none">
	<h4>Review Title...</h4>
	<p>Review Text...</p>
</div>
```

### Showing And Hiding On Click
```
const button = document.getElementById('see-review');

button.AddEventListener('click', function() {
	const review = document.getElementById('review');
	if (review.classList.contains('d-none')) {
		review.classList.remove('d-none');
	}
	else {
		review.classList.add('d-none');
	}
});
```

### Changing The Button Text On Click
```
const button = document.getElementById('see-review');

button.AddEventListener('click', function() {
	const review = document.getElementById('review');
	if (review.classList.contains('d-none')) {
		review.classList.remove('d-none');
		button.textContent = 'CLOSE REVIEW';
	}
	else {
		review.classList.add('d-none');
		button.textContent = 'SEE REVIEW';
	}
});
```