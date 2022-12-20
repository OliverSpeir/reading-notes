# Testing and Modules
- Testing is an important topic both in order to ensure sanity checks along development path and because most entry level jobs will start with writing tests
- Modules are important to understand because they are core to how python works

## References 
- [In Tests We Trust - TDD with Python](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)
- [If name equals main](https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/)
- [Recursion](https://www.geeksforgeeks.org/recursion/)
- [What on Earth is Recursion](https://www.youtube.com/watch?v=Mv9NEXX1VHc)
- [Python Modules and Packages Companion Video](https://realpython.com/courses/python-modules-packages/)
- [Google for Education: Python Lists](https://developers.google.com/edu/python/lists)
- [Google for Education: Python Strings](https://developers.google.com/edu/python/strings)
- [Python Modules and Packages](https://realpython.com/python-modules-packages/)
- [Python Scripts, Modules and Packages](https://realpython.com/lessons/scripts-modules-packages-and-libraries/)
- [Pytest Documentation](https://docs.pytest.org/en/latest/)
- [PyTest Tutorial](https://www.guru99.com/pytest-tutorial.html)
---
### [In Tests We Trust - TDD with Python](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)
- **TDD : Test Driven Development**
    - Write tests before code
- Unit tests are some pieces of code to exercise the input, output and behavior of your code
- Seperate test code from production code 
- test_moduleName.py is typical naming convention
- **AAA : Arrange, Act, Assert**
    - Arrange : organize the data needed to execute code
    - Act execute the code being tested
    - Assert check if the output is what was expected
- `pytest` is library to test
- **The Cycle**
    - Write unit test and make it fail (since no code written yet)
    - Write the feature and make it pass the test
    - Refactor the code (beautify)
- Writing tests forces us to think about the design first
- Come up with edge cases and test those
- [Test Driven Development by Example - Kent Beck PDF](https://docs.google.com/viewer?a=v&pid=sites&srcid=ZGVmYXVsdGRvbWFpbnx0ZXN0MTIzNHNpbTQ2NXxneDpiYTJmYWIwYTAyOGJiZmQ)
- [Growing Object-Oriented Software, Guided by Tests - Steve Freeman PDF](http://tisten.ir/wp-content/uploads/2018/11/Growing-Object-Oriented-Software-Guided-by-Tests.pdf)
---
### [If name equals main](https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/)
- Python interpreter reads source file and define special / global variables before executing code
- it sets the special `__name__` variable to have a value `"__main__"`
- If this file is being imported from another module, `__name__` will be set to the module’s name. Module’s name is available as value to `__name__` global variable. 
- A module is a file containing Python definitions and statements
```
print ("Always executed")
 
if __name__ == "__main__":
    print ("Executed when invoked directly")
else:
    print ("Executed when imported")
```
- All of the code that is at indentation level 0 [Block 1] gets executed every time
- When module is run directly aka `python script.py` code in if block[Block 2] will run because its name is main
- when module is run when its `__name__` is not `__main__` the else block [Block 2] will run
```
# How to run module by importing
if __name__ == "__main__":
    my_function()
 
import myscript
 
myscript.my_function()
```
- Python files can act as either reusable modules, or as standalone programs.
- if `__name__` == `“__main__”`: is used to execute some code only if the file was run directly, and not imported.
---
### [Recursion](https://www.geeksforgeeks.org/recursion/)
- when a function calls itself directly or indirectly this is called recursion
- Examples of problems solved by recursion
    - [Towers of Hanoi (TOH)](https://www.geeksforgeeks.org/c-program-for-tower-of-hanoi/)
    - [Inorder/Preorder/Postorder Tree Traversals](https://www.geeksforgeeks.org/tree-traversals-inorder-preorder-and-postorder/)
    - [DFS of Graph](https://www.geeksforgeeks.org/depth-first-traversal-for-a-graph/)
- It is essential to know that we should provide a certain case in order to terminate this recursion process. So we can say that every time the function calls itself with a simpler version of the original problem
    - Base Case and Recursive Case
- Recursion reduces code and makes it easier to read
- A task that can be defined with its similar subtask, recursion is one of the best solutions for it
    - Example factorial
 ```
  f(n) = 1 + 2 + 3 +……..+ n
   ```
``` 
f(n) = 1             n=1

f(n) = n + f(n-1)    n>1
```
- Recursion uses more memory
    - because func adds to the stack with each recursive call
    - LIFO (LAST IN FIRST OUT)
    - [Stack Data Structure](https://www.geeksforgeeks.org/stack-data-structure/)
- the solution to the base case is provided
```
int fact(int n)
{
    if (n < = 1) // base case
        return 1;
    else    
        return n*fact(n-1);    
}
```
- if base case is incorrect it will go forever
-  function is direct recursive if it calls itself
-  function is indriect recursion if it calls another function that calls it (either directly or indirectly) 
```
// An example of direct recursion
void directRecFun()
{
    // Some code....

    directRecFun();

    // Some code...
}

// An example of indirect recursion
void indirectRecFun1()
{
    // Some code...

    indirectRecFun2();

    // Some code...
}
void indirectRecFun2()
{
    // Some code...

    indirectRecFun1();

    // Some code...
}
```
- A recursive function is tail recursive when a recursive call is the last thing executed by the function.
    - [tail recursion article](https://www.geeksforgeeks.org/tail-recursion/)
- The memory per recursive call is allocated on top of memory allocated to the calling function and a different copy of local variables is created for each call.
- When the base case is reached, the function returns its value to the calling function and memory is de-allocated
- [Basic understanding of Recursion](https://www.geeksforgeeks.org/recursion/)


#### Fibonacci Example:
```
# Math Equation:
n if n == 0, n == 1;      
fib(n) = fib(n-1) + fib(n-2) otherwise;
```
```
# Recurrence Relation:
T(n) = T(n-1) + T(n-2) + O(1)
```
```
# Function for fibonacci
def fib(n):
 
    # Stop condition
    if (n == 0):
        return 0
 
    # Stop condition
    if (n == 1 or n == 2):
        return 1
 
    # Recursion function
    else:
        return (fib(n - 1) + fib(n - 2))
 
 
# Driver Code
 
# Initialize variable n.
n = 5;
print("Fibonacci series of 5 numbers is :",end=" ")
 
# for loop to print the fibonacci series.
for i in range(0,n):
    print(fib(i),end=" ")
```
