# Python Scope

- Scope is important to understand because it affects almost every block of code

## Resources

- [Python Scope](https://realpython.com/python-scope-legb-rule/)
- [Don’t be CONFUSED by BIG O notation anymore!](https://www.youtube.com/watch?v=5Uqawfl0VHQ)
- [Rolling Dice Examples](https://artofproblemsolving.com/wiki/index.php/Basic_Programming_With_Python#Program_Example_1_3)

## [Python Scope](https://realpython.com/python-scope-legb-rule/)

- scope rules how variables and names are looked up in your code
- It determines the visibility of a variable within the code
- The scope of a name or variable depends on the place in your code where you create that variable
- The Python scope concept is generally presented using a rule known as the LEGB rule
- Local, Enclosing, Global, and Built-in scopes
- Global scope: The names that you define in this scope are available to all your code
- Local scope: The names that you define in this scope are only available or visible to the code within the scope
- *Since Python is a dynamically-typed language, variables in Python come into existence when you first assign them a value*
    - [why python is dynamically typed](https://wiki.python.org/moin/Why%20is%20Python%20a%20dynamic%20language%20and%20also%20a%20strongly%20typed%20language)
- *Python scopes are implemented as dictionaries that map names to objects. These dictionaries are commonly called namespaces. These are the concrete mechanisms that Python uses to store names. They’re stored in a special attribute called .__dict__.*
  - variables are dictionaries !!
- Local (or function) scope is the code block or body of any Python function or lambda expression
  - The local scope or function scope is a Python scope created at function calls
- Enclosing (or nonlocal) scope is a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function
  - This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions
  - Names that you define in the enclosing Python scope are commonly known as nonlocal names
- Global (or module) scope is the top-most scope in a Python program, script, or module. 
- Built-in scope is a special Python scope that’s created or loaded whenever you run a script or open an interactive session
  - This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. It’s automatically loaded by Python when you run a program or script.
  - built-in scope is a special Python scope that’s implemented as a standard library module named builtins in Python 3.x. All of Python’s built-in objects live in this module.
- Can make what would otherwise be a local scoped variable global by using global statement
- Similarly to global names, nonlocal names can be accessed from inner functions, but not assigned or updated
- Closures are a special use case of the enclosing Python scope. When you handle a nested function as data, the statements that make up that function are packaged together with the environment in which they execute. The resulting object is known as a closure. In other words, a closure is an inner or nested function that carries information about its enclosing scope, even though this scope has completed its execution.
  - Closures provide a way to retain state information between function calls