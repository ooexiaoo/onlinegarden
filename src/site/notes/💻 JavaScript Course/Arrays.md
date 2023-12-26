---
{"dg-publish":true,"permalink":"/java-script-course/arrays/","dgPassFrontmatter":true,"noteIcon":"3","created":"2023-11-14T21:08:36.545+05:30","updated":"2023-12-11T19:08:07.541+05:30"}
---

🧶 Tags - #JavaScript 

---
🗃Resources - [[]]

---
🔗Links - https://app.pluralsight.com/course-player?clipId=0109e100-b1dd-402d-a82a-1a494eb35759

# [[💻 JavaScript Course/Arrays\|Arrays]]
==2023-01-07 - 15:03==

---
## Creating And Initializing Arrays
Arrays are objects that can hold multiple values or objects. To create an array, we simply use []

### Creating An Array
```
let values = [ ];
```

Because we are using [] the values will be in an array.

### Creating And Initialzing An Array
```
let values = [ 1, 2, 3, ];
```

Each item inside an array is called an **element**. So you can say values has 3 elements. This is the simplest way to create an array, but you can also create it with code.

### Initialze Using Array.of()
```
let values = Array.of(1, 2, 3);
```

### Making A Real Example
```JavaScript
const values = ['a', 'b', 'c'];

console.log(values);  // (3) ['a', 'b', 'c']
// 0: "a"
// 1: "b"
// 2: "c"
// length: 3

console.log(typeof values);  // object
console.log(Array.isArray(values));  //true
```

We can use any data type inside an array. In this example, we are using strings. We can even mix and match different data types inside an array, but it's best practice to always use the same data type.

Array is not a built-in data type, if we wanted to find out if a variable was an array, we can use **console.log(Array.isArray(values));

### Ref-Link - https://developer.mozilla.org

## Accessing Array Items
Array items are generally referred to as **elements**, but we might want to pull out an element to look at it, or we might want to change it.

### Accessing An Array
```
let values = ['a', 'b', 'c'];
console.log(values[0]);  //a
console.log(values[1]);  //b
console.log(values[2]);  //c
console.log(values[3]);  //undefined
```

To access the first element, we use [] on values and the index of **0**. Always remember that arrays are **0** based when it comes to indexing.

### Changing Values
```
const values = ['a', 'b', 'c'];
values[0] = 'aaa';
console.log(values[0]);  // aaa
```

We can change any value in the array using [] notation.

## Manipulating Arrays
Generally, arrays are manipulated by methods.

### Push()
```
const values =[ 'a', 'b', 'c'];
values.push('d');
console.log(values);  // a b c d
```

Push is a method that adds items to the end of the array.

### Pop()
```
const values = [ 'a', 'b', 'c'];
const last = values.pop();
console.log( last );  // c
```

Pop takes the last element off of an array.

### Shift()
```
const values = ['a', 'b', 'c'];
const first = values.shift();
console.log( first );  // a
```

Shift moves the entire array. You can think of shift as moving the entire array to the left one element and take the first value off the array.

### Unshift()
```
const values = [ 'b', 'c'];
value.unshift('a');
console.log( values );  // a b c
```

Unshift is the opposite of shift, as it adds things to the beginning of the array.

## Slice() And Splice()
There are more methods that are extremely common when working with arrays. **Slice** creates a brand-new array that's based on some original array. **Splice** is used to insert or delete elements somewhere within the array.

### Slice()
```
const values = ['a', 'b', 'c'];
const newValues = values.slice(1,2);
console.log( newValues );  // b
```

- When we execute **values.slice** we have 2 arguments.
- The 1st argument is where we want to start to take our slice. Which is **1** i.e, **b**.
- And 2 gives us the ending element that we want to look at. Which is **2** i.e, **c**.
- So **const newValues = values.slice(1,2);** creates a new array. And that new array is stored in the variable new values.

When we log out new value we get our slice which is **b** item **2** which is **'c'** is not included in the results. Even though we took our slice, it's important to remember that it left our original array the same. It essentially made a slice of the array without altering the original.

### Splice() For Deleting
```JavaScript
const values = ['a', 'b', 'c'];
values.splice(1, 1);
console.log( values );  // a c
```

- The 1st argument is the index we want to delete, i.e, **b**.
- The 2nd argument is the number of items we want to delete. i.e, just **1**.

Splice can also be used for inserting items.

### Splice() For Inserting
```
const values = [ 'a', 'b', 'c'];
values.splice(1, 0, 'foo');
console.log( values );  // a foo b c
```

* 1 refers to the index where we want to start **inserting** or **deleting**. i.e, between **a** and **b**.
* 0 specifies the number of items we want to delete. **0** means we don't want to delete anything, we just want to insert the new value. i.e, **foo**. If we specify 1, we'll delete one item, like we've seen in **splice() for deleting**.

## Array Searching And Looping
Many times we want to search through an array and find the index of some element. Sometimes this involves looping, some array methods will loop for you, but sometimes you want to get control over looping. You might want to perform some action at each element in an array. Or you might want to do a complex search and dig in through the element to find out what you're looking for by doing some kind of calculations to see if an element matches what you're looking for.

### IndexOf()
```
const values = ['a', 'b', 'c'];
console.log(values.indexOf('c'));  // 2
console.log(values.indexOf('d'));  // -1
```

**IndexOf** is a method that lets us get the index of a certain value in an array. When we search for something that doesn't exist, we get **-1**, it doesn't show us **undefined**. **-1** shows that we did the search and nothing came up.

## filter()
```
const values = ['a', 'b', 'c'];
const set = values.filter(function(item) {
	return item > 'b';
});
console.log(set);  // c
```

Filter method is another way to search through an array and creating a new array on values that fit some kind of criteria that you're looking for.

## find()
```
const values = ['a', 'bbb', 'c'];
const found = values.find(function(item) {
	return item.lenth > 1;
})
console.log( found );  // bbb
```

There is another similar method find, that'll look through each of the method array and find the first item that matches the criteria.

### forEach()
```JavaScript
const values = ['a', 'b', 'c'];
values.forEach(function(item) {
	console.log(item);
});
// a b c
```

**forEach** lets us execute a function on each element of an array. For each element in the array, this function is called once. 1st time it'll be set to **a**, then **b** and so on. We are simply logging out each item.

## Arrays In The DOM
When we're working with the DOM it's very common to use the arrays and array like objects.

### Getting Containers In The DOM
```
const container =
	document.getElementsByClassName('container');

console.log(container);  // HTMLCollection(8)
```

This returns something that's not officially an array, but it acts very much like one. We get an **HTML Collection** that is very similar to an array. **(8)** means it has 8 elements, there are 8 containers. When we open it in console, we can see all the containers present.

### Changing Class Attributes With Arrays
```
const container =
	document.getElementsByClassName('container');
containers[2].classList.add('d-none');  // d-none stands for display none
console.log(container);  // HTMLCollection(8)
```

We can use **container[2]** to, with [] having the number of container we want to manipulate to change the things we want in the container. In the example above, we just hide container 2. We can access all these elements because they are stored in this container's array.