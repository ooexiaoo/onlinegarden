---
{"dg-publish":true,"permalink":"/html-and-css/the-problem-with-view-points/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-11-14T21:08:36.691+05:30","updated":"2023-12-12T07:37:56.161+05:30"}
---

🧶 Tags - #HTML_CSS 

----
Resource - https://courses.kevinpowell.co/conquering-responsive-layouts

---
🔗 Links -
<center><iframe width="560" height="315" src="https://www.youtube.com/embed/veEqYQlfNx8?si=YX3MsJC01oO6ZMPf" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></center>
 
# [[🖥️ HTML & CSS/The Problem with View Points\|The Problem with View Points]]
==2023-08-26 - 22:47==

---
## DVH
A good alternative for **vh** is **dvh** which is dynamic view-port height. This can cause it's own issues as it will try to re-adjust when the height is less than, foe example 100vh, and try to adjust it back to 100vh when you scroll.

## SVH
**svh** is a small view-port height, that means that it'll try to assume that other elements will always be in view so, it will always be a bit smaller and will cover the rest of the space. So once you scroll and the other element disappears, we won't be at 100vh height anymore, but it is still better than **dvh** as it won't move around when scrolling.

Browser support for **svh** is still not there on all of these. So it's good to have both **vh** and **svh** in the css.
```css
height: 100vh;
height: 100svh;
position: relative;
```
