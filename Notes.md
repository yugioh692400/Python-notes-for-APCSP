# Python Notes
9/14/2026
# Setup (ignore this; I might have broken it)
1. Download Microsoft VS code and download the python extensions
<img width="2360" height="1323" alt="image" src="https://github.com/user-attachments/assets/4cb94725-930c-4276-9115-2a9483c4bfa6" />
2. Make a new file and name it Main or something similar followed by a .py (sets the language to python)
<img width="2360" height="1311" alt="image" src="https://github.com/user-attachments/assets/e55f8826-9deb-461a-a074-c1b322f4f0f5" />

# Stage 1

## 1.1 Your First Code
This is the most simple line of code you will ever run
```python
print(“Hello World”)
```
What each thing does

`print` send text into the terminal

`()` tells the code what to print

`””` makes the letters into text so they don’t seem like variables

## 1.2 Variables and Data Types
- Variable - a name that represents a value in a program
    - Can be assigned a value using the "=" operator
    - Can be used to store and manipulate data in a program
    - Can be used to make a program more readable and easier to understand by giving meaningful names to values
```python
age = 15 # I just made a Variable in which the age of someone is 15
```
   - Rules for naming variables:
     - Must start with a letter or underscore
     - Can contain letters, numbers, and underscores
     - Cannot be a reserved word in Python (such as "print" or "if")
     - Should be descriptive and meaningful to make the code easier to read and understand
     - Should use lowercase letters and underscores to separate words (snake_case) for variable names
     - Should use uppercase letters and underscores to separate words (UPPER_CASE) for constant variable names
```python
_Age_of_10th_Grader = 15 # good

/1 c * = 14 #bad
```
- String - a sequence of characters enclosed in quotes
  - `””`used to define a string
  - `’’` used to define a string"
  - Index starts at 0 and can be used to access specific characters in a string
  - `[start:stop:step]` Used to slice a string and extract a portion of it
    - Start - the index of the first character to include in the slice
    - Stop - the index of the first character to exclude from the slice
    - Step - the number of characters to skip between each character in the slice
  - `\n` is used to create a new line in a string
  - `\t` is used to create a tab space in a string
  - `.len()` is a function that returns the length of a string
  - `.upper()` is a method that returns a copy of the string with all characters converted to uppercase
  - Use the `+` operator to add strings together
    - Can also use the `+` operator to concatenate strings with other data types, but must convert the other data type to a string first using the `str()` function
  - `.format()` is a method that allows you to insert values into a string using placeholders
    - `{}` is used as a placeholder for a value to be inserted into the string
    - Use f-strings (formatted string literals) to insert values into a string using curly braces and the variable name

- List - creates a list of items
  - Can contain items of different data types
  - `[]` is used to define a list
  - Items in a list are ordered and can be accessed using their index
  - Items in a list can be changed, added, or removed
    - `.append()` is a method that adds an item to the end of a list
    - `.insert()` is a method that adds an item at a specific index in a list
    - `.remove()` is a method that removes the first occurrence of an item from a list
    - `.pop()` is a method that removes an item at a specific index from a list and returns it
    - `.len()` is a function that returns the number of items in a list
    - Can use the `+` operator to concatenate lists together
    - Can use `[start:stop:step]` to slice a list and extract a portion of it
      - Start - the index of the first item to include in the slice
      - Stop - the index of the first item to exclude from the slice
      - Step - the number of items to skip between each item in the slice
    - `.sort()` is a method that sorts the items in a list in ascending order
    - `.reverse()` is a method that reverses the order of the items in a list

- Dictionaries - a collection of key-value pairs
  - `{}` is used to define a dictionary
  - Key - a unique identifier for a value in the dictionary
  - Value - the data associated with a key in the dictionary
  - Can use the key to access the value in the dictionary
  - Good for storing and organizing data that has a relationship between keys and values
  - Good when you need to look up values based on a unique identifier
  - Add a string callback to the end of a dictionary to create a new key-value pair
  - Can use and data types as keys and values in a dictionary, but keys must be unique and immutable (cannot be changed)

- Tuples - a collection of items that are ordered and immutable (cannot be changed)
  - `()` is used to define a tuple
  - Items in a tuple are ordered and can be accessed using their index
  - Cannot change, add, or remove items from a tuple after it is created
  - Good for storing data that should not be changed, such as coordinates or dates
  - `.in()` is a keyword that checks if an item is in a tuple and returns True or False

- Sets - a collection of unique items that are unordered and mutable (can be changed)
  - `{}` is used to define a set
  - `.set()` is a function that creates a set from a list or other iterable
  - items in a set are unordered and cannot be accessed using an index
  - cannot have duplicate items in a set
  - good for storing data that should not have duplicates, such as a list of unique names
  - `.add()` is a method that adds an item to a set
  - `.remove()` is a method that removes an item from a set
    
- Boolean - a data type that can have one of two values: True or False
  - `True` is represents a value of 1
  - `False` is represents a value of 0
  - Used in conditional statements to control the flow of a program
  - ”T” in `True` and ”F” in `False` must be capitalized, otherwise it will return an error
  - `none` is a special value that represents the absence of a value or a null value

- Mathematical Operators - used to perform mathematical operations on numbers
    - `+` used to add 
    - `-` used to subtract
    - `*` used to multiply
    - `/` used to divide
    - `%` modulus (returns the remainder of a division operation)
    - `**` used for exponentiation (raises a number to a power)
    -  `//` used for floor division (returns the quotient of a division operation rounded down to the nearest whole number)

- Comparison Operators - used to compare two values and return a boolean value (True or False)
    - `==` equal to
    - `!=` not equal to
    -`>` greater than
    -`<` less than
    -`>=` greater than or equal to
    -`<=` less than or equal to

- If Statements - used to control the flow of a program based on a condition
    - `if` is used to check if a condition is true and execute a block of code if it is
    - `elif` is used to check if another condition is true if the previous condition was false
    - `else` is used to execute a block of code if all previous conditions were false
    - Can use comparison operators and boolean values in the condition of an if statement

- For Loops - used to iterate over a sequence of items and execute a block of code for each item
    - `for` is used to define a for loop
    - `in` is used to specify the sequence of items to iterate over
    - `range()` is a function that generates a sequence of numbers to iterate over
    - Statements:
        - `break` statement to exit a for loop early
        - `continue` statement to skip the current iteration of a for loop and move on to the next one
        - else statement with a for loop to execute a block of code after the loop has finished iterating over all items in the sequence
        - pass statement to create an empty block of code in a for loop or if statement
    - Functions:
        - `enumerate()` function to get the index and value of each item in a sequence while iterating over it in a for loop
        - `zip()` is a function to iterate over multiple sequences at the same time in a for loop
        - `reversed()` is a function to iterate over a sequence in reverse order in a for loop
        - `sorted()` is a function to iterate over a sequence in sorted order in a for loop
        - `list()` is a function to convert a sequence into a list while iterating over it in a for loop
        - `set()` is a function to convert a sequence into a set while iterating over it in a for loop
        - `dict()` is a function to convert a sequence of key-value pairs into a dictionary while iterating over it in a for loop
        - `any()`is a function to check if any item in a sequence meets a certain condition while iterating over it in a for loop
        - `all()` is a function to check if all items in a sequence meet a certain condition while iterating over it in a for loop
        - `filter()` is a function to create a new sequence of items that meet a certain condition while iterating over it in a for loop
        - `map()` is a function to create a new sequence of items by applying a function to each item in a sequence while iterating over it in a for loop
        - `reduce()` is a function from the functools module to apply a function cumulatively to the items in a sequence while iterating over it in a for loop
    - itertools module to create more complex iterators and generators while iterating over a sequence in a for loop

- While Loops - used to execute a block of code repeatedly while a condition is true
    - `while` is used to define a while loop
    - Can use comparison operators and boolean values in the condition of a while loop 
    - `break` statement to exit a while loop early
    - `continue` statement to skip the current iteration of a while loop and move on to the next one
    - `else` statement with a while loop to execute a block of code after the loop has finished iterating while the condition is false
    - `pass` statement to create an empty block of code in a while loop or if statement
    
- Functions - used to group a block of code together and give it a name so it can be reused multiple times
    - `def` is used to define a function
    - `function name` is a unique identifier for the function
    - parameters are values that are passed into a function when it is called
    - return statement is used to return a value from a function

- Error Types - different types of errors that can occur during the execution of a program
    - `SyntaxError` is occurs when there is a mistake in the syntax of the code
    - `NameError` is occurs when a variable or function is not defined
    - `TypeError` is occurs when an operation is performed on an object of an inappropriate type
    - `ValueError` is occurs when a function receives an argument of the correct type but an inappropriate value
    - `IndexError` is occurs when trying to access an index that is out of range for a sequence
    - `KeyError` is occurs when trying to access a key that does not exist in a dictionary
    - `AttributeError` is occurs when trying to access an attribute or method that does not exist for an object
    - `ImportError` is occurs when a module or library cannot be imported
    - `ZeroDivisionError` is occurs when trying to divide a number by zero
    - `FileNotFoundError` is occurs when trying to open a file that does not exist
    - `PermissionError` is occurs when trying to access a file or directory without the necessary permissions
    - `OSError` is occurs when a system-related error occurs, such as a file or directory not being found or a permission error
    - `ModuleNotFoundError` is occurs when a module cannot be found
    - `IndentationError` is occurs when there is an error in the indentation of the code
    - `TabError` is occurs when there is an error in the use of tabs and spaces for indentation in the code
    - `StopIteration` occurs when a generator or iterator has no more items to return
    - `KeyboardInterrupt` occurs when the user interrupts the execution of a program by pressing Ctrl+C or another interrupt signal
    - `SystemExit` occurs when the sys.exit() function is called to exit a program
    - `MemoryError` occurs when a program runs out of memory
    - `RecursionError` occurs when a function calls itself too many times and exceeds the maximum recursion depth
    - `FloatingPointError` is occurs when a floating-point operation fails, such as division by zero or overflow
    - `OverflowError` is occurs when a calculation exceeds the maximum limit for a numeric type
    
 - Warning Types - different types of warnings that can occur during the execution of a program   
    - `ImportWarning` is occurs when a module or library is imported that may cause compatibility issues with other modules or libraries
    - `ResourceWarning` is occurs when a resource, such as a file or network connection, is not properly closed or released
    - `RuntimeWarning` is occurs when a runtime issue is detected, such as a potential performance problem or a deprecated feature being used
    - `SyntaxWarning` is occurs when there is a potential issue with the syntax of the code that may cause unexpected behavior
    - `UserWarning` is occurs when a warning is issued to the user about a potential issue or problem with the code
    - `FutureWarning` is occurs when a feature or function is used that may be removed or changed in a future version of Python
    - `PendingDeprecationWarning` is occurs when a feature or function is marked for deprecation and may be removed in a future version of Python
    - `DeprecationWarning` is occurs when a feature or function is deprecated and may be removed in a future version of Python

- Error handling - used to handle errors that may occur during the execution of a program
    - `try` is used to define a block of code that may raise an error
    - `except` is used to define a block of code that will be executed if an error occurs in the try block
    - `finally` is used to define a block of code that will be executed regardless of whether an error occurred in the try block or not
    - `raise` is used to raise an error manually in a program
    - `assert` is used to check if a condition is true and raise an error if it is not
    - `with` is used to define a block of code that will automatically clean up resources when it is finished executing
    - `import` is used to import modules and libraries into a program
    - `as` is used to give a module or library a different name when it is imported into a program
    - `from` is used to import specific functions or classes from a module or library into a program
    - `pass` is used to create an empty block of code in a function or class
    - `docstring` is a string that is used to document a function or class and provide information about its purpose and usage
    - `help()` is a function that displays the docstring of a function or class and provides information about its purpose and usage
    - `dir()` is a function that displays a list of all the attributes and methods of an object or module
