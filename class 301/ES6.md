# Inheritance  
Inheritance is an important concept in object oriented programming. In the classical inheritance, methods from base class get copied into derived class.
In JavaScript, inheritance is supported by using prototype object.
For Eg: we have defined Person class (function) with FirstName & LastName properties and also added getFullName method to its prototype object.
```
function Person(firstName, lastName) {
    this.FirstName = firstName || "unknown";
    this.LastName = lastName || "unknown";
};

Person.prototype.getFullName = function () {
    return this.FirstName + " " + this.LastName;
}
```
Now, we want to create Student class that inherits from Person class so that we don't have to redefine FirstName, LastName and getFullName() method in Student class. The following is a Student class that inherits Person class.
```
function Student(firstName, lastName, schoolName, grade)
{
    Person.call(this, firstName, lastName);

    this.SchoolName = schoolName || "unknown";
    this.Grade = grade || 0;
}
//Student.prototype = Person.prototype;
Student.prototype = new Person();
Student.prototype.constructor = Student;
```
Please note that we have set Student.prototype to newly created person object. The new keyword creates an object of Person class and also assigns Person.prototype to new object's prototype object and then finally assigns newly created object to Student.prototype object. Optionally, you can also assign Person.prototype to Student.prototype object.
Now, we can create an object of Student that uses properties and methods of the Person as shown below.
```
function Person(firstName, lastName) {
    this.FirstName = firstName || "unknown";
    this.LastName = lastName || "unknown";            
}

Person.prototype.getFullName = function () {
    return this.FirstName + " " + this.LastName;
}
function Student(firstName, lastName, schoolName, grade)
{
    Person.call(this, firstName, lastName);

    this.SchoolName = schoolName || "unknown";
    this.Grade = grade || 0;
}
//Student.prototype = Person.prototype;
Student.prototype = new Person();
Student.prototype.constructor = Student;

var std = new Student("James","Bond", "XYZ", 10);
            
alert(std.getFullName()); // James Bond
alert(std instanceof Student); // true
alert(std instanceof Person); // true
```
Thus we can implement inheritance in JavaScript.

# MDN this  
A function's this keyword behaves a little differently in JavaScript compared to other languages. It also has some differences between strict mode and non-strict mode.
In most cases, the value of this is determined by how a function is called (runtime binding). It can't be set by assignment during execution, and it may be different each time the function is called. ES5 introduced the bind() method to set the value of a function's this regardless of how it's called, and ES2015 introduced arrow functions which don't provide their own this binding (it retains the this value of the enclosing lexical context).
```
const test = {
  prop: 42,
  func: function() {
    return this.prop;
  },
};

console.log(test.func());
// expected output: 42
```
[Source](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
# MDN class  
Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.
The basic syntax is:
```
class MyClass {
  // class methods
  constructor() { ... }
  method1() { ... }
  method2() { ... }
  method3() { ... }
  ...
}
```
Then use new MyClass() to create a new object with all the listed methods.

The constructor() method is called automatically by new, so we can initialize the object there.

For example:
```
class User {

  constructor(name) {
    this.name = name;
  }

  sayHi() {
    alert(this.name);
  }

}

// Usage:
let user = new User("John");
user.sayHi();
```
[Source](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
