# Data Analysis

## Resources

- [JuptyerLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html)
- [NumPy](https://www.dataquest.io/blog/numpy-tutorial-python/)
- [NumPy Tutorial](https://www.tutorialspoint.com/numpy/index.htm)
- [Numpy Cheat Sheet](https://s3.amazonaws.com/dq-blog-files/numpy-cheat-sheet.pdf)

## [JuptyerLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html)

- JupyterLab is a next-generation web-based user interface for Project Jupyter.

## [NumPy](https://www.dataquest.io/blog/numpy-tutorial-python/)

- NumPy is a commonly used Python data analysis package.
- NumPy was originally developed in the mid 2000s
- Can be used to make csv data more usable by making it more readable with built in methods
- numpy can read files 
- numpy has builtin array methods 
    - its own type of array
        - its own type of slicing its own arrays etc
- N dimensional numpy arrays are much easier to work with
- You can use the `numpy.ndarray.astype` method to convert an array to a different type
- array math:
    - If you do any of the basic mathematical operations (/, *, -, +, ^) with an array and a value, it will apply the operation to each of the elements in the array. 
- can do operations between arrays as well like divide one array by another

- Broadcasting
    - Unless the arrays that you’re operating on are the exact same size, it’s not possible to do elementwise operations. In cases like this, NumPy performs broadcasting to try to match up elements. Essentially, broadcasting involves a few steps:

- NumPy Array Comparisons
    - NumPy makes it possible to test to see if rows match certain values using mathematical comparison operations
- Subsetting
    - return array elements conditionally like SQL queries in a way
- can reshape arrays while keeping all elements
- can combine arrays 
