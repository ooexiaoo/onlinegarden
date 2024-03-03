---
{"dg-publish":true,"permalink":"/coding/next-js/react-server-components-rsc/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-03-03T21:32:43.942+05:30","updated":"2024-03-03T21:41:53.996+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[💻 Coding/Next.js/Routing\|Routing]]
Down:: [[💻 Coding/Next.js/Introduction to Next.js\|Introduction to Next.js]]
🗃 Resources:: [Playlist](https://www.youtube.com/watch?v=x7oQC_R_yVo&list=PLC3y8-rFHvwjOKd6gdf4QtV1uYNiQnruI&index=4)
==2024-03-03 - 21:32==

React Server Component is a new architecture introduced by the React team in version 18 which was quickly embraced by Next.js.
The architecture introduces a new way of creating React components, splitting them into two types:
- Server components
- Client components

## React Server Components Contd.
### Server Components
- In Next.js, all components are Server components by default
- They have the ability to run tasks like reading files or fetching data from a database
- However, they don't have the ability to use hooks or handle user interactions
### Client Components
- To create a Client component, it's necessary to add **"use client"** at the top of the component file
- Client components can't perform tasks like reading files, but they have the ability to use hooks and manage interactions