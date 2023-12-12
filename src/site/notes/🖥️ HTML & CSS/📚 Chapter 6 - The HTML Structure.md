---
{"dg-publish":true,"permalink":"/html-and-css/chapter-6-the-html-structure/","noteIcon":"1"}
---

 🧶 Tags - #HTML_CSS 

---
 Resources - [[]]
 
---
 Links - https://github.com/SuperSimpleDev/html-css-course-2022/tree/main/1-exercise-solutions/lesson-06

Using a proper HTML structure tells the browser what we exactly want to show. If we are now using the right HTML structure, we can lose some key features and the browser may not show our code as we intend it to.
![Pasted image 20221105185351.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Pasted%20image%2020221105185351.png)
```
1 - <!DOCTYPE html>
This shows that we want the latest version of html to be used to show our website. Without this our code can get messed up.

2 - <html></html>
All our html code will be inside these tags only. This element represents the entire webpage.

3 - <Head></head>
	<body></body>
These are the head and body elements in which we use different types of code specific to the data we want to give to the browser.

Usually anything is the head is not supposed to be shown on the page, Like anayltics code/tracking code, etc. You can also move all the CSS code in the head, but commonly this is not not because it make the code confusing and its not a good practice to mix to different languages together.

Example - <title>Site Name</title>

4 - <html>
	<head></head>
	<body></body>
	</html>
Putting elements inside other elements is called 'nesting.'

5a - We use a .CSS file for all the CSS code and link the file with <link> element. This element does not have a closing tag like the usual tags. This kinds of tags are called 'void elements.'

- To link CSS file to the html we'll use <link rel="stylesheet" href="buttons.css"

The benefits of doing this is each file contains less code and each file contains the same type of code.

5b - When we use 'href' tag for CSS the computer will search for the file right besides the HTML file you're writing the code in. So it makes sense to keep the HTML & CSS files in the same folder with no other files with the same name in the folder.

But you can add neighboring folders with the right names like -
<link rel="stylesheet" href="style/buttons.css"

6 - We can also load new fonts from the internet with right into the head tag of our site to use it in our website.

Example - We can go to https://fonts.google.com/ to choose different styles google then gives us 2 codes one for the head section and other for the CSS file. Using these we can embed any font that we want.

Summary - Features we get from following a proper HTML stucture
	1. <title>
	2. Live Server
	3. Link CSS Files
	4. Add New Fonts
	5. and more...
```

# Void elements = No closing tag

-   `area` - clickable, defined area in an image
-   `base` - specifies a base URL from which all links base
-   `br` - line break
-   `col` - column in a table (deprecated)
-   `hr` - horizontal rule (line)
-   `img` - image
-   `input` - field where users enter data
-   `link` - links an external resource to the document
-   `meta` - provides information about the document
-   `param` - defines parameters for plugins

HTML 5 standards include all non-deprecated tags from the previous list and

-   `command` - represents a command users can invoke (obsolete)
-   `keygen` - facilitates public key generation for web certificates (deprecated)
-   `source` - specifies media sources for `picture`, `audio`, and `video` elements.


In HTML5, the following elements are void:

-   `area`
-   `base`
-   `br`
-   `col`
-   `embed`
-   `hr`
-   `img`
-   `input`
-   `keygen`
-   `link`
-   `meta`
-   `param`
-   `source`
-   `track`
-   `wbr`

# Exercise 6d -
![Screenshot_1 5.png](/img/user/Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/Screenshot_1%205.png)

## HTML
```
<!DOCTYPE html>

<html>

<head>

<title>Model 3</title>

<link rel="stylesheet" href="model3.css">

<link rel="preconnect" href="https://fonts.googleapis.com">

<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">

</head>

<body>

<p class="model3">Model 3</p>

<p class="linked">Order Online for <span class="touch">Touchless Delivery</span></p>

</body>

</html>
```

## CSS
```
* {font-family: 'Montserrat', sans-serif;

padding: 0;

}

p{

text-align: center;

}

.model3{

text-align: center;

font-size: 40px;

font-weight: bold;

line-height: 20px;

}

.linked{

font-weight: 500;

}

.touch{

text-decoration: underline;

cursor: pointer;

}
```