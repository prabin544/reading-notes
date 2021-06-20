## FileIO & Exceptions

#### Read & Write Files in Python  
File is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.  
When we want to work with a file, the first thing to do is to open it. This is done by invoking the open() built-in function. open() has a single required argument that is the path to the file. open() has a single return, the file object:  
```
file = open('dog_breeds.txt')
```
The with statement automatically takes care of closing the file once it leaves the with block, even in cases of error. Highly recommended is that we use the with statement as much as possible, as it allows for cleaner code and makes handling any unexpected errors easier for us.  
```
with open('dog_breeds.txt', 'r') as reader:
```
Most likely, we will also want to use the second positional argument, mode.  

'r'	 --> Open for reading (default)  
'w'	 --> Open for writing, truncating (overwriting) the file first  
'rb' or 'wb'	--> Open in binary mode (read/write using byte data)  

```
# using with statement
with open('file_path', 'w') as file:
    file.write('hello world !')
```

## Exceptions in Python

Exception occurs whenever syntactically correct Python code results in an error. For Eg:  
```
>>> print( 0 / 0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: integer division or modulo by zero
```
#### Handling an Exception  
It is possible to write programs that handle selected exceptions. Look at the following example, which asks the user for input until a valid integer has been entered, but allows the user to interrupt the program (using Control-C or whatever the operating system supports); note that a user-generated interruption is signalled by raising the KeyboardInterrupt exception.
```
>>> while True:
...     try:
...         x = int(input("Please enter a number: "))
...         break
...     except ValueError:
...         print("Oops!  That was no valid number.  Try again...")
```



