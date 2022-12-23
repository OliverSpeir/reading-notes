# Classes, Objects, Recursion, and Pytest
- Core functionality of python and programming in general

## Resources
- [Classes and Objects](https://www.learnpython.org/en/Classes_and_Objects)
- [Thinking Recursively](https://realpython.com/python-thinking-recursively/)
- [Pytest Fixtures and Coverage](https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage)
- [Pytest Fixtures](https://docs.pytest.org/en/latest/fixture.html)

### [Classes and Objects](https://www.learnpython.org/en/Classes_and_Objects)
- Objects are an encapsulation of variables and functions in a single entity
    - objects get their variables and functions from classes
        - classes are template you create to create your objects
            - (similar to JS)
```
class ExampleClass:
    variable = "xyz"

    def function(self):
        print("lmnop")

example_object_x = ExampleClass()
example_object_y = ExampleClass()
example_object_y.variable = "abc"
example_object_x.function()
```
- `__init__()` function is special function that is called when class is being initiated
    - it is used for assigning values in a class
```
class NumberHolder:

   def __init__(self, number):
       self.number = number

   def returnNumber(self):
       return self.number

var = NumberHolder(7)
print(var.returnNumber())
#Prints '7'
```

### [Thinking Recursively](https://realpython.com/python-thinking-recursively/)
- Recursive Functions
- Recursive Data Structures
- maintaining state during recursion and avoiding recomputation by cachin results 
    - [caching results](https://realpython.com/python-memcache-efficient-caching/)

<img src = "https://i.imgur.com/9GBmsFw.png"/>

- Example of "typical" recursive algorithm 

```
a recursive function will continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: base case and recursive case. 
```

- Maintaining State
    - Each recursive function has its own execution context
        - In order to maintain state:
            - Thread the state through each recursive call so that the current state is part of the current calls execution context (scope)
            - keep the state in global scope
            - [threading explain](https://realpython.com/intro-to-python-threading/)
```
# Thread state through each call
def sum_recursive(current_number, accumulated_sum):
    # Base case
    # Return the final state
    if current_number == 11:
        return accumulated_sum

    # Recursive case
    # Thread the state through the recursive call
    else:
        return sum_recursive(current_number + 1, accumulated_sum + current_number)
```
<img src = "https://i.imgur.com/MOz4nYH.png"/>

```
# Global mutable state
current_number = 1
accumulated_sum = 0


def sum_recursive():
    global current_number
    global accumulated_sum
    # Base case
    if current_number == 11:
        return accumulated_sum
    # Recursive case
    else:
        accumulated_sum = accumulated_sum + current_number
        current_number = current_number + 1
        return sum_recursive()
```

- Recursive Data Structure
    - A data structure is recursive if it can be deﬁned in terms of a smaller version of itself
        - list in python is example
```
# Return a new list that is the result of
# adding element to the head (i.e. front) of input_list
def attach_head(element, input_list):
    return [element] + input_list

```
```
attach_head(1,                                                  # Will return [1, 46, -31, "hello"]
            attach_head(46,                                     # Will return [46, -31, "hello"]
                        attach_head(-31,                        # Will return [-31, "hello"]
                                    attach_head("hello", [])))) # Will return ["hello"]
```

<img src = "https://files.realpython.com/media/list.3df62a89243d.gif"/>

- We apply a function to an argument, then pass that result on as an argument to a second application of the same function, and so on. Repeatedly composing attach_head with itself is the same as attach_head calling itself repeatedly.
- Fibbonacci Example for Cacheing
  - `Fn = Fn-1 + Fn-2`
  - ` F0 = 0 and F1 = 1 ` = base case

- no cache:

``` python
>>> fibonacci_recursive(5)
Calculating F(5), Calculating F(4), Calculating F(3), Calculating F(2), Calculating F(1), 
Calculating F(0), Calculating F(1), Calculating F(2), Calculating F(1), Calculating F(0), 
Calculating F(3), Calculating F(2), Calculating F(1), Calculating F(0), Calculating F(1),
```
   
 - with cache: 
```
>>> fibonacci_recursive(5)
Calculating F(5), Calculating F(4), Calculating F(3), Calculating F(2), Calculating F(1), Calculating F(0),
```

- only difference between functions: 

```
from functools import lru_cache

@lru_cache(maxsize=None)
def fibonacci_recursive(n):
```
- Python does not support tail-call elimination
    - [Wikipedia for Tail Call](https://en.wikipedia.org/wiki/Tail_call)
    - You can cause stack overflow by using more stack frames than the default call stack depth
        - [Default Call Stack Depth PyDoc](https://docs.python.org/3.6/library/sys.html#sys.getrecursionlimit)
        - ``` >>> import sys
              >>> sys.getrecursionlimit() 

- Also, Python’s mutable data structures don’t support structural sharing, so treating them like immutable data structures is going to negatively affect your space and GC (garbage collection) efficiency because you are going to end up unnecessarily copying a lot of mutable objects

### [Pytest Fixtures](https://docs.pytest.org/en/latest/fixture.html)

- Fixtures are objects available to all of your tests
    - might contain data you want to share across tests, or they might involve the network or filesystem

- you can define fixtures using a combination of the pytest.fixture decorator

-  fixtures are used differently from global variables
    - can set scope by `@pytest.fixture(scope='module')`
        - module scope is not suggested
- Coverage 
    - 100% code coverage doesn't mean that your code is perfect or that it lacks bugs. But it does give you a greater degree of confidence
    -  pytest-cov
        - coverage html
- [py test docs](http://pytest.org.)
- [python testing book](http://pythontesting.net.)