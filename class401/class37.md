## ES6 Syntax and Feature Overview

#### Variable declaration
```
let x = 0
```
#### Constant declaration
```
const CONST_IDENTIFIER = 0
```
#### Arrow functions
```
let func = (a) => {} // parentheses optional with one parameter
let func = (a, b, c) => {} // parentheses required with multiple parameters
```
#### Template literals
```
let str = `Release Date: ${date}`
```
#### Multi-line strings
```
let str = `This text
            is on
            multiple lines`
```
#### Implicit returns
```
let func = (a, b, c) => a + b + c // curly brackets must be omitted
```
#### Key/property shorthand
```
let obj = {
  a,
  b,
}
```
#### Method definition shorthand
```
let obj = {
  a(c, d) {},
  b(e, f) {},
}
```
#### Destructuring (object matching)
```
let {a, b, c} = obj
```
#### Array iteration (looping)
```
for (let i of arr) {
  console.log(i)
}
```
#### Default parameters
```
let func = (a, b = 2) => {
  return a + b
}
```
```
func(10) // returns 12
func(10, 5) // returns 15
```
Spread syntax
Spread syntax can be used to expand an array.

ES6
```
let arr1 = [1, 2, 3]
let arr2 = ['a', 'b', 'c']
let arr3 = [...arr1, ...arr2]

console.log(arr3) // [1, 2, 3, "a", "b", "c"]
```
Spread syntax can be used for function arguments.

ES6
```
let arr1 = [1, 2, 3]
let func = (a, b, c) => a + b + c

console.log(func(...arr1)) // 6
```
#### Classes/constructor functions
ES6 introducess the class syntax on top of the prototype-based constructor function.


ES6
```
class Func {
  constructor(a, b) {
    this.a = a
    this.b = b
  }

  getSum() {
    return this.a + this.b
  }
}

let x = new Func(3, 4)
```
```
x.getSum() // returns 7
```

#### Inheritance
The extends keyword creates a subclass.


ES6
```
class Inheritance extends Func {
  constructor(a, b, c) {
    super(a, b)

    this.c = c
  }

  getProduct() {
    return this.a * this.b * this.c
  }
}

let y = new Inheritance(3, 4, 5)
```
```
y.getProduct() // 60
```

#### Modules - export/import
Modules can be created to export and import code between files.

index.html
```
<script src="export.js"></script>
<script type="module" src="import.js"></script>
```
export.js
```
let func = (a) => a + a
let obj = {}
let x = 0

export {func, obj, x}
```
import.js
```
import {func, obj, x} from './export.js'

console.log(func(3), obj, x)
```

#### Promises/Callbacks
Promises represent the completion of an asynchronous function. They can be used as an alternative to chaining functions.


ES6 Promise
```
let doSecond = () => {
  console.log('Do second.')
}

let doFirst = new Promise((resolve, reject) => {
  setTimeout(() => {
    console.log('Do first.')

    resolve()
  }, 500)
})

doFirst.then(doSecond)
```
An example below using XMLHttpRequest, for demonstrative purposes only (Fetch API would be the proper modern API to use).


ES6 Promise
```
function makeRequest(method, url) {
  return new Promise((resolve, reject) => {
    let request = new XMLHttpRequest()

    request.open(method, url)
    request.onload = resolve
    request.onerror = reject
    request.send()
  })
}

makeRequest('GET', 'https://url.json')
  .then((event) => {
    console.log(event.target.response)
  })
  .catch((err) => {
    throw new Error(err)
  })
```
            
