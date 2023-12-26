---
{"dg-publish":true,"permalink":"/java-script-course/program-flow/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-11-14T21:08:36.540+05:30","updated":"2023-12-12T07:35:06.493+05:30"}
---

🧶 Tags - #JavaScript 

---
🗃Resources - [[]]

---
🔗Links - https://app.pluralsight.com/course-player?clipId=9a678f6d-e96e-41dd-884f-56998b4d0993

# [[💻 JavaScript Course/Program Flow\|Program Flow]]
==2022-12-29 - 08:37==

---
In JavaScript, sometimes we have to conditionally execute some code blocks, but if the condition is not fulfilled we don't.

We do this by adding **if** statement and in parentheses we put the conditions **(5 === 5)** if the condition is true we execute the code block, in this case it's the code in the parentheses **{}**.

In the example below, we are working with numbers, but in most cases we'll be working with variables as shown in the second example.

## Conditionals Using if()
```
if (5 === 5){          //true
console.log('Yes');
}

if (5 > 10){          //false
console.log('No');
}

if (5 >= 5){          //true
console.log('Yes');
}
```

```
let state = "FL";
let taxPercent = 0;

if (state !== "FL"){       // not equal
	taxPercent = 7;
}

console.log(taxPercent);    // 7
```
---
## Truthy & Falsy

|                         |                      |
| ----------------------- | -------------------- |
| falsy                   | truthy               |
| false                   | Everything NOT falsy |
| 0                       | true                 |
| "" or " (empty strings) | 0.5                  |
| null                    | "0"                  |
| undefined               |                      |
| NaN                     |                      |

```
if (1.1 + 1.3 !== 2.4){
	showMessage('true');
}
```
In this example, the answer will not be equal to 2.4 as JavaScript uses in accurate floating point numbers.

The way to fix this by rounding off your numbers -
One way to do that is by adding parentheses, by adding parentheses we can treat it as an object.
We can also add **.toFixed(2)** by adding 2 we get 2 decimal places, which can be rounded off.

The problem with adding .toFixed is that it returns a string. We need to convert all of this from a string to a number. The easiest way to do that is by adding a **+** before the parentheses. Think of the **plus sign** as similar to the **negative sign**

**-** will make the number negative, but **+** leaves the number as it is, but it does have the benefit of converting the string to a number.

When you're working with floating point numbers, you always need to convert them to a fixed amount of decimal places if you're comparing them to a literal, such as 2.4.

```
if ( +(1.1 + 1.3).toFixed(2) !== 2.4){
	showMessage('true');
}
```

We can also add as many lines of code as we'd like between the opening and closing parentheses.
We can also put **if statements** inside other if statements.
```
if ( +(1.1 + 1.3).toFixed(2) !== 2.4){
	let message = 'hello';
	showMessage(message);
}
```

## If () ... Else

### Example 1
```
let state = "FL";
let taxPercent = 0;

if (state === "FL"){       
	taxPercent = 7;
}
else {
	taxPercent = 0;
}

console.log(taxPercent);    // 7
```

We can also add **else if** statements like the example below, these types of constructs are pretty common in JavaScript. We can put as many **else's and else if's** as we like
### Example 2
```
let state = "FL";
let taxPercent = 0;

if (state === "FL"){       
	taxPercent = 7;
}
else if (state === 'NY'){
	taxPercent = 8.875;
}

console.log(taxPercent);    // 7
```

## Comparing === and ==
```
if (1 === "1"){
	showMessage('true');
}
else {
	showMessage('false');
}
```
The above code will give the result **if else**, as one is not equal to a string.
However, if we use a == the result will be **true** as JavaScript will try to convert **types**, I.e, A number into a string. This can lead to a lot of confusion at times.

It's a best practice to compare **same type** to avoid any confusion. Which is why we use === instead of ==

Sometimes the === is read as **strictly equal to** or **identically equal to,** and that's because the types need to be the same.

Likewise, there is a not equal to symbol !== and != which act the same as === and ==

| Sign | Meaning             |
| ---- | ------------------- |
| ===  | Identically Equal to  |
| ==   | Is Equal to       |
| !===  | Identically Unequal to|
| !==     | Is Unequal to                   |

## The Ternary Operator
```
// (condition) ? true-statement : false-statement;

let message = (price > 10) ? 'expensive' : 'cheap';
showMessage(message); /expensive
```

The question mark acts like the question.
The 1st option is a placeholder for a true statement.
The 2nd option is a placeholder for a false statement.

As in the above example, the answer will come to expensive if the price is greater than 10 if not it'll show the message cheap.

```
let price = 20;
(price > 10) ? showMessage('yes') : showMessage('no');
price > 10 ? showMessage('yes') : showMessage('no');   //Parentheses are not necessary, but is a best practice.
```

```
let price = 20;
let message = (price > 10) ? 'yes' : 'no';
showMessage(message);
```

## Block Scope Using Let
A block of code exists between the opening and closing parentheses, and we can declare variables within a block. So if we declare a variable using **let, or const**, that variable will be only available in the block.

```
if (true) {
	let value = 'yes';
	showMessage(value);
}
console.log(value);
```

When we use console.log we will see an error as the value is declared in a code block, and we won't be able to declare it with console.log. This is one way we can encapsulate the code and not leak it outside the code block.

This doesn't work with the old keyword **var**. as this is considered an old practice. This will leak the code outside the code block, making it harder to debug and can cause a lot of confusion.

```
if (true) {
	var value = 'yes';   //not a best practice
	showMessage(value);
}
console.log(value);
```

## Looping With For ()
We've seen several ways to conditionally execute code, that will either execute the code or skip it all together, but sometimes we need to loop over code. We need to execute the same code over and over and over.

We can do this with the **for** statement
```
for (let i = 0; i , 3; i++) {
console.log(i);
}

// 0 1 2
```

1. The keyword **for** lets us create a loop.
2. Then we have a statement in the opening and closing parentheses, **let i = 0;**. Here we're declaring a new variable **i**, and we're setting it to **0** and this is the first thing that executes in a loop.
3.  Next, we have a condition **i < 3;** where we see is **i** is less than **3**. And if this is true, then we execute this loop. The body of the loop being **console.log(i);**
4. The final part **i++** is the statement that will execute after the loop completes. (The **++** operator is the increment operator, where it adds **1 to i**)

One thing that you can mess up is that you can create an infinite loop by mistake, which will make the page unresponsive and even the browser and the loop will never finish executing.

> Always make sure the loop finishes executing at some point, as it can hang the browser and even the server if the code goes into an infinite loop.

```
for (let i = 0; i , 3; i--) {
console.log(i);
}
```

Let's say for example we write **i--** instead of **i++** this will decrement **i**, so the condition will always be true, **i** will always be less than **5** and the loop will never stop executing.

## While () Loop
```
let count = 1;
while (count <5) {
console.log(count);
count++;
}
// 1 2 3 4
```
Just like the **for** loop, we set the **while** keyword and specify a condition **(count < 5)**

> **i** is a traditional variable used in loops that stands for **Index or Iterator**, but you'll often see names like **i, j, x, y, z** used in loops.

### Another Example
```
let i = 4;
while(i > 0) {
console.log(i);
i--;
}
```

## Looping With Do ... While()
You use do while loop when you're sure that the body of the code will run at least once.

```
let count = 1;
do {
	console.log(count);
	count++;
} while (count < 5);
// 1 2 3 4
```

### Another Example
```
let = 4;
do {
	console.log(i);
	i--;
} while (i > 0);
// 4 3 2 1
```
If we use **-4** instead of **4** the code will just log **-4** and stop as **-4** is less than **0**. The code will then continue to execute from the next block.