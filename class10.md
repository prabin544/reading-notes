# JavaScript Call Stack
A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.
```
function greeting(name) {
  alert('Hello ' + name);
}

function processUserInput(callback) {
  var name = prompt('Please enter your name.');
  callback(name);
}

processUserInput(greeting);
```
In Asynchronous JavaScript, we have a callback function, an event loop, and a task queue. The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.
Basically a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).

### How does the call stack handle function calls?
We will answer this question by looking at a sample code of a function that calls another function. Here is the example code:
```
function firstFunction(){
  console.log("Hello from firstFunction");
}

function secondFunction(){
  firstFunction();
  console.log("The end from secondFunction");
}

secondFunction();
```

# JavaScript error messages && debugging
Errors can be categorized into 4 different type:  

## Reference errors
When there is missing variable defined.
```
console.log(foo) // Uncaught ReferenceError: foo is not defined
```
OR
```
foo = 'Hello' // Uncaught ReferenceError: foo is not defined
let foo
```
## Syntax errors
This occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.
```
JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1
```
## Range errors
Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.
```
var foo= []
foo.length = foo.length -1 // Uncaught RangeError: Invalid array length
```
## Type errors
This types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.
```
var foo = {}
foo.bar // undefined
foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined
```
# Debugging
The debugger statement invokes any available debugging functionality, such as setting a breakpoint. If no debugging functionality is available, this statement has no effect.
```
function potentiallyBuggyCode() {
    debugger;
    // do potentially buggy stuff to examine, step through, etc.
}
```
## Best Ways to Debug JavaScript.
- console.log() - write any message or piece of information to the console
- console.debug() - very similar to console.log, but is used for browser compatibility and by default .debug messages are hidden in some browsers.
- console.warn - has a different type of output message, and is typically used for less-critical pieces of information.
- console.info() - almost identical to console.log()
- console.error() - should be reserved for more serious issues and actual errors. This method is what automatically captures exceptions and other JavaScript issues. 
