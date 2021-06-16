### Classes and Objects
#### Classes
Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects.
```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")
 ```
 
 Assigining class to object:
 ```
 class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass()
 ```
 #### Accessing Object Variables
 ```
 class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass()

myobjectx.variable
 ```
 ### Recursive Functions in Python
 A recursive function is a function defined in terms of itself via self-referential expressions.
 ```
 def factorial_recursive(n):
    # Base case: 1! = 1
    if n == 1:
        return 1

    # Recursive case: n! = n * (n-1)!
    else:
        return n * factorial_recursive(n-1)
 ```
 ### Pytest Fixtures and Coverage
 In pytest, you define fixtures using a combination of the pytest.fixture decorator, along with a function definition. 
 ```
 @pytest.fixture(scope='module')
def simple_file():
   return StringIO('\n'.join(['abc', 'def', 'ghi', 'jkl']))
```

 
