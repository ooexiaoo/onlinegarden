---
{"wordcount":0,"dg-publish":true,"permalink":"/coding/react-js-notes/react-component-lifecycle/","dgPassFrontmatter":true,"noteIcon":"3","created":"2024-02-28T17:03:12.312+05:30","updated":"2024-02-28T17:24:09.252+05:30"}
---

🧶 Tags:: #ReactJs #Code 
🗃 Resources:: [YouTube](https://www.youtube.com/watch?v=abjeWy4sZiU&list=PLu0W_9lII9agx66oZnT6IyhcMIbUMNMdt&index=34) | [wejtekmaj Diagram](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/)
==2024-02-28 - 17:03==

The series of events that happen from the mounting of a React component to its unmounting.
**Mounting:** Birth of your component.
**Update:** Growth of your component.
**Unmount:** Death of your component.


![reactjs component life cycle.png](/img/user/%F0%9F%9B%A2%EF%B8%8F%20Resources/%F0%9F%93%81%20Files/%F0%9F%93%B8Images/reactjs%20component%20life%20cycle.png)
## While Mounting
In this case, the ‘Constructor’ runs first after that the ‘render’ lifecycle method is invoked. After that, React will update the DOM and finally, the ComponentDidMount will be executed.

## While Updating
The three possible ways in which one can update the React component are:
1. New props
2. Using setState
3. Using forceupdate()

After updating the component, the render method will be executed at the start. After that react updates the "DOM and references" and in the end, the componentDidUpdate method will be run.

## While Unmounting
At the time of unmounting, only the componentWillUnmount method will be executed and the component will be unmounted.