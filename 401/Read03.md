# FileIO & Exceptions
- Important because advantage and functionality of python is ability to re-use files as functions(modules) or standalone scripts
- Exceptions are important to understand in terms of debugging
## Resources
- [Read & Write Files in Python](https://realpython.com/read-write-files-python/)
- [Exceptions in Python](https://realpython.com/python-exceptions/)
- [Read & Write Files in Python - Companion Video](https://realpython.com/courses/reading-and-writing-files-python/)
- [Reading and Writing Files in Python Quiz](https://realpython.com/quizzes/read-write-files-python/)
- [Real Python Cheat Sheet (I got click-baited so you dont have to)](https://static.realpython.com/python-cheat-sheet.pdf)


## [Read & Write Files in Python](https://realpython.com/read-write-files-python/)
- **What is a file?**
  - contiguous set of bytes 
    - these bytes become binary
  - Most files have:
    - Header: metadata about contents (name,type,etc)
    - data: contents
    - end of file (EOF): special character that denotes end
  - Line ending
    - Line ending dates back to morse code
    - ISO ASA standardized how lines should be ended
      - either CR or LF
    - Windows uses CR+LF
    - Unix uses LF
  - Character encoding
    - encoding is translation of byte data to human readable characters
      - ASCII or UNICODE (UTF-8)
        - ASCII is subset of UTF-8
        - ASCII is 128 characters
        - UTF-8 is ~1m
- **Working with files**
  - open(/path) builtin function
    - single req arg : filepath
  - always need to close files 
    - [Why Is It Important to Close Files in Python?](https://realpython.com/why-close-file-python/)
    - resources leaks etc
  - convention to either use with block or try-finally block to open file that will close it automatically
    - with automatically closes when script exits block
    - try finally needs to have the finally written (which could be forgotten)
  - with open ('path', parameter)
    - parameters: 
      - -r : open to read
      - -w open to write
      - rb or wb opens in binary mode
  - File Object
    - A file object is:
        “an object exposing a file-oriented API (with methods such as read() or write()) to an underlying resource.” 
            - [PyDocs - Term: File Object](https://docs.python.org/3/glossary.html#term-file-object)
    - 3 different categories of file objects
      - Text
      - Buffered Binary
      - Raw Binary
      - Deeper explanation: [PyDocs - io (core tool)](https://docs.python.org/3/library/io.html)
    - Text file type
      - open('path') open('path', 'r') or open('path', 'w')
        - returns _io.TextIOWrapper
    - Buffered Binary File
      - open('abc.txt', 'rb') or open('abc.txt', 'wb')
        - returns _io.BufferedReader
    - Raw File Type
      - Not used in high level language typically
      - open('abc.txt', 'rb', buffering=0)
        - returns _io.FileIO
  - Read File:
    - .read(size=-1) reads entire file returns a string (size is variable meaning # of char read)
    - .readline(size=-1) reads line size is how many char into line
    - .readlines() reads remaining lines from file object and returns them as list
    ```
      # iterate over each line of file
      with open('abc.txt', 'r') as reader:
        for line in reader:
           print(line, end='')
    ```
  - Write to File:
    - write(string)
    - or open in append mode with 'a'
    ```
    with open('abc.txt', 'a') as a_writer:
      a_writer.write('xyz')
    ```
  - `__file__`
    - The `__file__` attribute is a special attribute of modules, similar to `__name__`
      - “the pathname of the file from which the module was loaded, if it was loaded from a file.”
        - [Data Model PyDocs](https://docs.python.org/3/reference/datamodel.html)
  - File as class
    ```
      class my_file_reader():
      def __init__(self, file_path):
          self.__path = file_path
          self.__file_object = None
  
      def __enter__(self):
          self.__file_object = open(self.__path)
          return self
  
      def __exit__(self, type, val, tb):
          self.__file_object.close()
      ```
  - most file types have modules for them
    - [Reading and Writing CSV Files in Python](https://realpython.com/python-csv/)
    - [Working With JSON Data in Python](https://realpython.com/python-json/)
  
## [Exceptions in Python](https://realpython.com/python-exceptions/)
  - Python programs terminate as soon as they encouter errors
    - Error could be syntax error or exception
  - Syntax error occurs when parser detects incorrect statement
  - Exception error message includes what type of exception 
  - Can use `raise` to throw exception based on condition 
    - `raise Exception('error message')
  - can use `assert` in similar way
    - assert (condition), "AssertionError Exception message"
  - try except block can be used as error handling
    - try 
      - run code
    - except
      - run code if there is an exception
    - make assertion then have try except following that and if the assertion is false it won't shut down program
      - assertionerror exception message will print in stdout as well as except code block running
      - function name that was affect will also print
    - [PyDocs built in exceptions](https://docs.python.org/3/library/exceptions.html)
    - Be specific about except blocks because things can get buried if there are a lot of functions in try
      - [tutorial about specific except classes](https://realpython.com/the-most-diabolical-python-antipattern/)
    - can do try except else blocks
      - except only runs if there is an exception
    - can do try except else finally blocks
      - finally always runs at end

 [Read & Write Files in Python - Companion Video](https://realpython.com/courses/reading-and-writing-files-python/)
  - after 2nd less videos are paylocked 
    - appear to reiterate article directly