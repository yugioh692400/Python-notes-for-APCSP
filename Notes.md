# Python Notes
9/14/2026
# Setup
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
  - `\n` - used to create a new line in a string
  - `\t` - used to create a tab space in a string
  - `.len()` - a function that returns the length of a string
  - `.upper()` - a method that returns a copy of the string with all characters converted to uppercase
  - Use the `+` operator to add strings together
    - Can also use the `+` operator to concatenate strings with other data types, but must convert the other data type to a string first using the `str()` function
  - `.format()` - a method that allows you to insert values into a string using placeholders
    - `{}` - used as a placeholder for a value to be inserted into the string
    - Use f-strings (formatted string literals) to insert values into a string using curly braces and the variable name

- List - creates a list of items
  - Can contain items of different data types
  - `[]` - used to define a list
  - Items in a list are ordered and can be accessed using their index
  - Items in a list can be changed, added, or removed
    - `.append()` - a method that adds an item to the end of a list
    - `.insert()` - a method that adds an item at a specific index in a list
    - `.remove()` - a method that removes the first occurrence of an item from a list
    - `.pop()` - a method that removes an item at a specific index from a list and returns it
    - `.len()` - a function that returns the number of items in a list
    - Can use the `+` operator to concatenate lists together
    - Can use `[start:stop:step]` to slice a list and extract a portion of it
      - Start - the index of the first item to include in the slice
      - Stop - the index of the first item to exclude from the slice
      - Step - the number of items to skip between each item in the slice
    - `.sort()` - a method that sorts the items in a list in ascending order
    - `.reverse()` - a method that reverses the order of the items in a list

- Dictionaries - a collection of key-value pairs
  - `{}` - used to define a dictionary
  - Key - a unique identifier for a value in the dictionary
  - Value - the data associated with a key in the dictionary
  - Can use the key to access the value in the dictionary
  - Good for storing and organizing data that has a relationship between keys and values
  - Good when you need to look up values based on a unique identifier
  - Add a string callback to the end of a dictionary to create a new key-value pair
  - Can use and data types as keys and values in a dictionary, but keys must be unique and immutable (cannot be changed)

- Tuples - a collection of items that are ordered and immutable (cannot be changed)
  - `()` - used to define a tuple
  - Items in a tuple are ordered and can be accessed using their index
  - Cannot change, add, or remove items from a tuple after it is created
  - Good for storing data that should not be changed, such as coordinates or dates
  - `.in()` - a keyword that checks if an item is in a tuple and returns True or False

- Sets - a collection of unique items that are unordered and mutable (can be changed)
  - `{}` - used to define a set
  - `.set()` - a function that creates a set from a list or other iterable
  - items in a set are unordered and cannot be accessed using an index
  - cannot have duplicate items in a set
  - good for storing data that should not have duplicates, such as a list of unique names
  - `.add()` - a method that adds an item to a set
  - `.remove()` - a method that removes an item from a set
    
- Boolean - a data type that can have one of two values: True or False
  - `True` - represents a value of 1
  - `False` - represents a value of 0
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

#Comparison Operators - used to compare two values and return a boolean value (True or False)
    - `==` equal to
    - `!=` not equal to
    -`>` greater than
    -`<` less than
    -`>=` greater than or equal to
    -`<=` less than or equal to
