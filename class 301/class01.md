# Introduction to React and Components

## What is React.js?
 
React.js is an open-source JavaScript library that is used for building user interfaces specifically for single-page applications. It’s used for handling the view layer for web and mobile apps. React also allows us to create reusable UI components. React was first created by Jordan Walke, a software engineer working for Facebook. React first deployed on Facebook’s newsfeed in 2011 and on Instagram.com in 2012.
 
React allows developers to create large web applications that can change data, without reloading the page. The main purpose of React is to be fast, scalable, and simple. It works only on user interfaces in the application. This corresponds to the view in the MVC template. It can be used with a combination of other JavaScript libraries or frameworks, such as Angular JS in MVC.

[Source](https://reactjs.org/)
 
React JS is also called simply to React or React.js.  

## Hello World
```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

### Introducing JSX
JSX produces React “elements”. React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both. We will come back to components in a further section, but if you’re not yet comfortable putting markup in JS, this talk might convince you otherwise.

React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.

### JSX Syntax
```
const element = <h1>Hello, world!</h1>;
```
### Rendering elements
```
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```
### Components and props
Components in React are independent, reusable pieces of UI. A typical web page may consist of a navbar, content area & footer. In React, we create these areas as components (which in turn may consist of other components!). It saves on code duplication & as we’ll see, allows for an immense amount of flexibility.
React Props are like function arguments in JavaScript and attributes in HTML.

[Source](https://reactjs.org/docs/introducing-jsx.html)
