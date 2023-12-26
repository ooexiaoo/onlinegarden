---
{"dg-publish":true,"permalink":"/java-script-course/functions/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-11-14T21:08:36.526+05:30","updated":"2023-12-11T19:36:56.392+05:30"}
---

🧶 Tags - #JavaScript 

---
🗃Resources - [[]]

---
🔗Links -

# [[💻 JavaScript Course/Functions\|Functions]]
==2023-01-02 - 11:20==

---
A function is a block of code that's named, you can use that name or a variable that points to that function.

If you're not writing the code inside a function, then you're writing the code inside the global scope, which is pretty limited. Most of the code that you write, you'd want them to be reusable within functions.

## Function Basics
One way to look at functions is that a function is a block of code with a name and because it has a name you can call it over and over. Most of the JavaScript code that you write will be within functions.

### Basic Function Code Format
```
function showMessage() {

}
```

* **function** - We use the function keyword.
* **showMessage** - We give it a name.
* **()** - We follow that with opening and closing parentheses. 
* **{}** - We have opening and closing curly braces. Whatever is within these curly braces is referred to as the body of the function.


```
function showMessage() {
	console.log('in a function');
}
```

We can have anything code in the body, we can have **if statements, loops, we can call other functions, and we can even call ourselves as a function**.

We can call a function in a simple way like this -
We can call a function as many times as we want.
```
function showMessage() {
	console.log('in a function');
}
showMessage();

showMessage();

// the message is shown twice
```

## Function Expressions
There's another popular way to declare a function and immediately store it in a variable. These are called function expressions.

```
function showMessage() {  // function delcaration

}
let fn = function () {   // function expression

}
fn();    // calls the function
```

* We create a function with the **function** variable.
* All this gets assigned to a variable using the **let** statement.
* So **fn** is our new variable name, which stands for function.
* To call this function, we simply use the variable **fn();**

These are 2 common ways to define functions, function declaration and function expression.

```
let myFunction = function () {
	console.log('Here is a message');
}

myFunction();
```

You don't need to give the function a name, but giving a name will make debugging it easier.

```
let myFunction = function loggingFunction () {   // with name
	console.log('Here is a message');
}

myFunction();
```

## Passing Information To Functions
It's very useful to be able to pass information into a function, that way the function can work with whatever data you send it.

```
function showMessage(message) {
	console.log(message);
}

showMessage('First Message');
showMessage('Second Message');
```

So we're declaring a function **showMessage**, but this time between the opening and closing parentheses we have a function parameter **(message)**, we can think of this as a variable. Whatever information we pass through this function will be stored in **(message)**.

```
function showMessage(message, anotherMessage) {
	console.log(message, anotherMessage);
}
showMessage('First Message', 'Second Message');
```

We can pass multiple types of values and information through a function just by listing several parameters separated by commas.

```
let myFunction = function (message, firstName) {
	console.log(message);
	console.log(firstName);
}

myFunction('Hello', 'John');
```

## Function Return Values
Above we saw when we create a function, we can specify parameters and those are symbols representing information coming into the function. We can also get information out of the function by using the return keyword. The function may or may not return a value.

### Example 1
```
function getSecretCode(value) {
	let code = value * 42;
	return code;
}

console.log( getSecretCode(2));   // 84
```

* In **getSecretCode, (value)** became 2.
* **code** became 2 * 42, which is 84.
* Then we returned **code**, the variable.

If we forget to add **return code,** we'll get an error undefined. If a function does not have a return statement, it implicitly returns undefined.

### Example 2
```
function getSecretCode(value) {
	// let code = value * 42;
	return value * 42;
}

console.log( getSecretCode(2));   // 84
```

We can also do it like this, and it really depends on your own coding style how you want to do it.
But the first example looks cleaner and is easier to follow.

### Example 3
```
function getSecretCode(value) {
	let code = value * 42;
	return code;
}

let secretCode = getSecretCode(2);
console.log( secretCode );   // 84
```

In example 3 we made it look cleaner by creating a good variable name called **secretCode** and dividing the code into 2 lines instead of one. This maybe more preferred than putting the function call right in **console.log**.

## Function Scope
Functions have their own scope, that means that the parameters and the local variables to that function only exist within that function and sub functions. Once the function finishes execution and parameters or local variables disappear.

### Example 1
```
function getSecretCode(value) {
	let code = value * 42;
	return code;
}

let secretCode = getSecretCode(2);
console.log( code );
// return Error: code is undefined
```

In this example 1, we can see that once the code finishes execution, we can't use **console.log (code)** to get the value of **code**, as JavaScript has no idea that **code** even existed. We call this being out of scope.

All functions have a scope and this is a good thing because then the code can't leak out into the surrounding code.

### Example 2
```
let key = 42;                  // defined outside the function

function getSecretCode(value) {
	let code = value * key;
	return code;
}

let secretCode = getSecretCode(2);
console.log( secretCode );

// 84
```

Functions have access to outer code as long there is a variable or something defined outside the function, any newly declared functions can use it, but of course this doesn't work the other way. Once the function finishes execution, the local variable **code** no longer exists.

You might very often see nested functions, Like CSS, these are functions inside other functions.

### Example 3
```
let key = 42;                  // defined outside the function

function getSecretCode(value) {
	
	let keyGenerator = function() {    // Nested function
		let key = 12;
		console.log('in keyGenerator:', key);
		return key;
	}
	 
	let code = value * keyGenerator();
	console.log(' in getSecretCode:', key);
	return code;
}

let secretCode = getSecretCode(2);
console.log( secretCode );

// in keyGenerator: 12  - Nested Function
// in keyGenerator: 42
```

In example 3 we can see that once the nested function completes its execution the value of **key** which is **12** no longer exists, therefore when the main function executes we get the answer **42** which we defined outside the function like in example 2.

So you always need to be aware of function scope as we're using the same variable name in more than one place. And if we use the same variable name inside the function, it will override any function name outside the function.

Key takeaway, Once the function finishes it's executing all of its local variables will disappear and if something is declared in the global scope it will always stick around because it's the most outermost scope.

## Using Functions To Modify Web Pages

### JavaScript
```
function showMessage(message) {
	document.getElementById('message').textContent = message;
}
function changePercentOff(percentage) {
	document.getElementById('percent-off').textContent = percentage + "% OFF";
}
changePercentOff ( 30 );
```
### HTML
```
<h1> id="message" class="col-sm-12">GET A GRIP</h1>
<h2> id="percent-off">20% OFF</h2>
```

* **Document** is an object that refers to the whole page.
* We specify "**.**" on the object and call a special kind of function on that object.
* You can think **getElementById** as a function, and we're a message.
* Then access the text content of the object and we get it to **message** our parameter.