---
{"dg-publish":true,"permalink":"/java-script-course/variables-and-values/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-11-14T21:08:36.564+05:30","updated":"2023-12-12T07:35:15.365+05:30"}
---

🧶 Tags - #JavaScript 

---
🗃Resources - [[]]
 
---
🔗Links -
 
# [[💻 JavaScript Course/Variables & Values\|Variables & Values]]
==2022-11-19 - 22:39==

Variables are like containers. You can save a value inside a variable.
![Pasted image 20221119224932.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Pasted%20image%2020221119224932.png)
---
```
<script>

let todo1 = 'get groceries';

let todo2 = 'wash car';

let todo3 = 'make dinner';

</script>
```
So when we go to the console and type <mark style="background: #FF5582A6;">'console.log(todo1);'</mark> it gives us the output <mark style="background: #BBFABBA6;">'get groceries.'</mark>
But if we do the same thing by adding quotes to todo1, <mark style="background: #FF5582A6;">'console.log('todo1');'</mark> it gives us the out of <mark style="background: #BBFABBA6;">'todo1'.</mark>

todo1 is a variable, a container which will log the value inside the variable. But todo1 with quotes around it is not a variable anymore, it's an actual value.

todo1 is a string which we can see by typing in the console 'typeof' which will give us the output of 'string'

---
# Exercise 3 -
```
<script>

let month = 'November';

let day = '20';

let year = '2022';

</script>

<script>

let age = '28';

let message = 'Iam' + age + 'years old';

</script>
```