### In Tests We Trust - TDD with Python
Test-driven development is a software development process relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases.  
[source](https://en.wikipedia.org/wiki/Test-driven_development)

- The greatest advantage about TDD is to craft the software design first
- Your code will be more reliable: after a change you can run your tests and be in peace
- Beginning may be hard — and that’s fine. You just need to practice!  

When we are writing tests we are forced to think about the design first and how we can break it into small pieces.

### Recursion  
The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. Using recursive algorithm, certain problems can be solved quite easily.  
In the recursive program, the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems as such. 
``` 
int fact(int n)
{
    if (n < = 1) // base case
        return 1;
    else    
        return n*fact(n-1);    
}
```

A problem is solved using recursive function by breaking larger problem into small and adding one or more base conditions that would stop the recursion.
[source](https://www.geeksforgeeks.org/recursion/)
