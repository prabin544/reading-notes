# Functional Programming Concepts
Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data — Wikipedia

### A pure function is a function which:
- Given the same inputs, always returns the same output, and
- Has no side-effects

### Function composition
- Is the process of combining two or more functions in order to produce a new function or perform some computation.

### Immutability
- An immutable object is an object that can’t be modified after it’s created. Conversely, a mutable object is any object which can be modified after it’s created.

### Side Effects
A side effect is any application state change that is observable outside the called function other than its return value. Side effects include:
- Modifying any external variable or object property (e.g., a global variable, or a variable in the parent function scope chain)
- Logging to the console
- Writing to the screen
- Writing to a file
- Writing to the network
- Triggering any external process
- Calling any other functions with side-effects

### Functional programming favors:
- Pure functions instead of shared state & side effects
- Immutability over mutable data
- Function composition over imperative flow control
- Lots of generic, reusable utilities that use higher order functions to act on many data types instead of methods that only operate on their colocated data
- Declarative rather than imperative code (what to do, rather than how to do it)
- Expressions over statements
- Containers & higher order functions over ad-hoc polymorphism  

[Source](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

# Refactoring Javascript for Readability
Code refactoring is defined as the process of restructuring computer code without changing or adding to its external behavior and functionality.

### Best practices for code refactoring
- Refactor first before adding any new features
- Plan your refactoring project and timeline carefully
- Test often
- Focus on progress, not perfection
- Try refactoring automation  
[Source](https://www.altexsoft.com/blog/engineering/code-refactoring-best-practices-when-and-when-not-to-do-it/)
