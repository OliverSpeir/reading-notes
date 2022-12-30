# Ten Thousand Part 3

## Resources

[List Comprehensions](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)
[Debugging with PySnooper](https://www.pythonpodcast.com/pysnooper-python-debugging-episode-241/)
[Primer on Decorators](https://realpython.com/primer-on-python-decorators/)

## [List Comprehensions](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)

- 3 core steps of list comprehension
    1. First is the expression we’d like to carry out. expression inside the square brackets.
    2. Second is the object that the expression will work on. item inside the square brackets.
    3. Finally, we need an iterable list of objects to build our new list from. list inside the square brackets.
- isdigit()
    - gets only numbers using conditional 
        - [ x for x in iterable if x.isdigit()]
- Can parse files this way
    - lines = [ line for line in file ]
- Expressions can be functions
    ```
    def double(x):
        return x*2

    nums = [double(x) for x in range(1,10)]
    ```
## [Primer on Decorators](https://realpython.com/primer-on-python-decorators/)
- Put simply: decorators wrap a function, modifying its behavior.
- Decorators provide a simple syntax for calling higher-order functions.
- In Python, functions are first-class objects. This means that functions can be passed around and used as arguments
- It’s possible to define functions inside other functions.
- Python also allows you to use functions as return values
    - can either invoke them or just use the reference 

- Simple Decorator:
```
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

def say_whee():
    print("Whee!")

say_whee = my_decorator(say_whee)
>>> say_whee()
Something is happening before the function is called.
Whee!
Something is happening after the function is called.
```
- Syntactic Sugar
    - Python allows you to use decorators in a simpler way with the @ symbol,
```
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

@my_decorator
def say_whee():
    print("Whee!")
```
- Decorators can be moved into own module then imported
- Decorating Functions With Arguments
    - *args and **kwargs 
        - allows decorator to accept arbitrary number of positional and keyword arguments
```
def do_twice(func):
    def wrapper_do_twice(*args, **kwargs):
        func(*args, **kwargs)
        func(*args, **kwargs)
    return wrapper_do_twice
    
@do_twice
def greet(name):
    print(f"Hello {name}")
```