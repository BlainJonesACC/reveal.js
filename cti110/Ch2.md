# Chapter 2

## Software Development, Data Types, and Expressions

### Fundamentals of Python: First Programs Second Edition

---

## Objectives (1 of 2)

2.1 Describe the basic phases of software development: analysis, design, coding, and testing
2.2 Use strings for the terminal input and output of text
2.3 Use integers and floating point numbers in arithmetic operations
2.4 Construct arithmetic expressions
2.5 Initialize and use variables with appropriate names

---

## Objectives (2 of 2)

2.6 Import functions from library modules
2.7 Call functions with arguments and use returned values appropriately
2.8 Construct a simple Python program that performs inputs, calculations, and outputs
2.9 Use docstrings to document Python programs

---

## The Software Development Process (1 of 4)

* **Software development:** process of planning and organizing a program
  * Several approaches; one is the **waterfall model**
* Waterfall model phases:
  * Customer request
  * Analysis
  * Design
  * Implementation
  * Integration
  * Maintenance
* Modern software development is usually **incremental** and **iterative**
  * Analysis and design may produce a **prototype** of a system for coding, and then back up to earlier phases to fill in more details after some testing

---

## The Software Development Process (2 of 4)

---

## The Software Development Process (3 of 4)

* Programs rarely work as hoped the first time they are run
* Must perform extensive and careful testing
* The cost of developing software is not spread equally over the phases

---

## The Software Development Process (4 of 4)

---

## Strings, Assignment, and Comments

* Text processing is by far the most common application of computing
* E-mail, text messaging, Web pages, and word processing all rely on and manipulate data consisting of strings of characters

---

## Data Types (1 of 2)

* A **data type** consists of a set of values and a set of operations that can be performed on those values
* A **literal** is the way a value of a data type looks to a programmer
* **int** and **float** are **numeric data types**
* They represent numbers

---

## Data Types (2 of 2)

---

## String Literals (1 of 2)

* In Python, a string literal is a sequence of characters enclosed in single or double quotation marks
* '' and "" represent the empty string
* Double-quoted strings are handy for composing strings that contain single quotation marks or apostrophes:

    ```text
    >>>  “I’m using a single quote in this string!”
    “I’m using a single quote in this string!”
    >>>  print(“I’m using a single quote in this string!”)
    I’m using a single quote in this string!
    ```

---

## String Literals (2 of 2)

* Use ‘‘‘ and ”””for multi-line paragraphs

    ```text
    >>>  print(“””This very long sentence extends
    all the way to the next line.”””)
    This very long sentence extends all the way to the next line
    ```

* When you evaluate a string in Python without the print function
  * You can see the literal for the newline character, \n embedded in the result:
  
    ```text
    >>> “””This very long sentence extends
    all the way to the next line.”””
    ‘This very long sentence extends\nall the way to the next line.’
    ```

---

## Escape Sequences

* The newline character \n is called an escape sequence

---

## String Concatenation

* You can join two or more strings to form a new string using the concatenation operator **+**

    ```text
    >>> “Hi “ + “there,” + “Ken!”
    ‘Hi there, Ken!
    ```

* The **\*** operator allows you to build a string by repeating another string a given number of times

    ```text
    >>> “ “ * 10 + “Python”
    ‘          Python’
    ```

---

## Variables and the Assignment Statement (1 of 3)

* A variable associates a name with a value
  * Makes it easy to remember and use later in program
* Variable naming rules:
  * Reserved words cannot be used as variable names
    * Examples: **if**, **def**, and **import**
  * Name must begin with a letter or _
  * Name can contain any number of letters, digits, or _
  * Names are case sensitive
    * Example: WEIGHT is different from weight
  * Tip:  begin each word in the variable name with an uppercase, except the first one (Example: interestRate)

---

## Variables and the Assignment Statement (2 of 3)

* Programmers use all uppercase letters for **symbolic constants** (contain values that the program never changes)
  * Examples: **TAX_RATE** and **STANDARD_DEDUCTION**
* Variables receive initial values and can be reset to new values with an **assignment statement**

    ```python
    <variable name> = <expression>
    ```

--

* Subsequent uses of the variable name in expressions are known as variable references

    ```text
    >>> firstName = “Ken”
    >>> secondName = “Lambert”
    >>> fullName = firstName + “ ” + secondName
    >>> fullName
    ‘Ken Lambert’
    ```

---

## Variables and the Assignment Statement (3 of 3)

* Variables serves two purposes:
  * Help the programmer keep track of data that change over time
  * Allow the programmer to refer to a complex piece of information with a simple name (called abstraction)

---

## Program Comments and Doc strings (1 of 3)

* Program comments
  * A piece of program text that the computer ignores but that provides useful documentation to programmers

--

* Docstring
  * A multi-line string of the form

```python [1,9|2|3|4|6-8]
"""
Program: circle.py
Author: Ken Lambert
Last date modified: 10/10/17

The purpose of this program is to compute the area of a circle. The input is an integer or 
floating-point number representing the radius of the circle. The output is a floating-point 
number labeled as the area of the circle.
"""
```

---

## Program Comments and Doc strings (2 of 3)

* End-of-line comments
  * Begin with the # symbol and extend to the end of a line
  * Might explain the purpose of a variable or the strategy used by a piece of code
  * Example:

    ```python
    RATE = 0.85 # Conversion rate for Canadian to US dollars
    ```

---

## Program Comments and Doc strings (3 of 3)

* Tips related to comments and doc strings:
  * Begin a program with a statement of purpose and other information helpful to programmers
  * Accompany a variable definition with a comment that explains the variable’s purpose
  * Precede major segments of code with brief comments that explain their purpose
  * Include comments to explain the workings of complex or tricky sections of code

---

## Numeric Data Types and Character Sets

* The first applications of computers were to crunch numbers

* The use of numbers in many applications is still very important

---

## Integers

* In real life, the range of **integers** is infinite
* A computer’s memory places a limit on the magnitude of the largest positive and negative integers
* Python’s **int** typical range:
  * $-21^{31}$ to $21^{31}$
* Integer literals are written without commas

---

## Floating-Point Numbers (1 of 2)

* Real numbers have **infinite precision**
  * The digits in the fractional part can continue forever
* Python uses **floating-point** numbers to represent real numbers
* Python’s **float** typical range:
  * $-10^{308}$ to $10^{308}$ and
  * Typical precision: 16 digits

---

## Floating-Point Numbers (2 of 2)

* A floating-point number can be written using either ordinary **decimal notation** or **scientific notation**

---

## Character Sets

* In Python, character literals look just like string literals and are of the string type
  * They belong to several different **character sets**, among them the **ASCII set** and the **Unicode set**
* ASCII character set maps to a set of integers
* **ord** and **chr** functions convert characters to and from ASCII

    ```text
    >>> ord(‘a’)
    97
    >>> ord(‘A’)
    65
    >>> chr(65)
    ‘A’
    >>> chr(66)
    ‘B’
    ```

---

## Expressions

* A literal evaluates to itself
* A variable reference evaluates to the variable’s current value
* **Expressions** provide easy way to perform operations on data values to produce other values
* When entered at Python shell prompt:
  * an expression’s operands are evaluated
  * its operator is then applied to these values to compute the value of the expression

---

## Arithmetic Expressions (1 of 3)

* An arithmetic expression consists of operands and operators combined in a manner that is already familiar to you from learning algebra

---

## Arithmetic Expressions (2 of 3)

* **Precedence rules:**
  * ** has the highest precedence and is evaluated first
  * Unary negation is evaluated next
  * *, /, and % are evaluated before + and −
  * \+ and − are evaluated before =
  * With two exceptions, operations of equal precedence are **left associative**, so they are evaluated from left to right
    * \** and = are **right associative**
  * You can use () to change the order of evaluation

---

## Arithmetic Expressions (3 of 3)

* When both operands of an expression are of the same numeric type, the resulting value is also of that type
* When each operand is of a different type, the resulting value is of the more general type
* Example: **3 / 4** is 0, whereas **3 / 4.0** is .75
* For multi-line expressions, use a \
* Example:

    ```text
    >>> 3 + 4 * \
    2 ** 5
    131
    ```

---

## Mixed-Mode Arithmetic and Type Conversions (1 of 4)

* Mixed-mode arithmetic involves integers and floating-point numbers:

    ```text
    >>> 3.14 * 3 ** 2
    28.26
    ```

  * You must use a type conversion function when working with input of numbers
  * It is a function with the same name as the data type to which it converts
* Input function returns a string as its value
  * You must use the int or float function to convert the string to a number before performing arithmetic

---

## Mixed-Mode Arithmetic and Type Conversions (2 of 4)

---

## Mixed-Mode Arithmetic and Type Conversions (3 of 4)

* Note that the int function converts a float to an int by truncation, not by rounding

    ```text
    >>> int(6.75)
    6
    >>> round(6.75)
    7
    ```

---

## Mixed-Mode Arithmetic and Type Conversions (4 of 4)

* Type conversion also occurs in the construction of strings from numbers and other strings

    ```text
    >>> profit = 1000.55
    >>> print(‘$’ + profit)

    Traceback (most recent call last):
    File “<stdin>”, line 1, in <module>
    TypeError: cannot concatenate ‘str’ and ‘float’ objects
    ```

* Solution: use str function

    ```text
    >>> print(‘$’ + str(profit))
    $1000.55
    ```

* Python is a strongly typed programming language

---

## Using Functions and Modules

* Python includes many useful functions, which are organized in libraries of code called modules

---

## Calling Functions: Arguments and Return Values

* A function is chunk of code that can be called by name to perform a task
* Functions often require arguments or parameters
  * Arguments may be optional or required
* When function completes its task, it may return a value back to the part of the program that called it
* To learn how to use a function’s arguments, use the help function:

    ```text
    >>> help(round)
    Help on built-in function round in module builtin:
    round(…)
    round(number[, n digits]) -> floating point number
    Round a number to a given precision in decimal digits (default 0 digits).
    This returns an int when called with one argument, otherwise the same type as
    number, n digits may be negative.
    ```

---

## The Math Module (1 of 2)

* Functions and other resources are coded in components called **modules**
* Functions like **abs** and **round** from the _builtin_ module are always available to use
* The math module includes functions that perform basic mathematical operations
* To use a resource from a module, you write the name of a module as a qualifier, followed by a dot (.) and the name of the resource
  * Example: **math.pi**

    ```text
    >>> math.pi
    3.1415926535897931
    Math.sqrt(2)
    1.4142135623730951
    ```

---

## The Math Module (2 of 2)

* You can avoid the use of the qualifier with each reference by importing the individual resources

    ```text
    >>> from math import pi, sqrt
    >>>print(pi, sqrt(2))
    3.14159265359 1.41421356237
    ```

* You may import all of a module’s resources to use without the qualifier
  * Example:

    ```python
    from math import *
    ```

---

## The Main Module

* In the case study, earlier in this chapter, we showed how to write documentation for a Python script
* To differentiate this script from the other modules in a program, we call it the main module
  * Like any module, the main module can be imported
  
    ```text
    >>> import taxform
    Enter the gross income: 120000
    Enter the number of dependents: 2
    The income tax is $20800.0
    ```

* After importing a main module, view its documentation by running the help function

---

## Program Format and Structure

* Start with comment with author’s name, purpose of program, and other relevant information
  * In a doc string
* Then, include statements that:
  * Import any modules needed by program
  * Initialize important variables, suitably commented
  * Prompt the user for input data and save the input data in variables
  * Process the inputs to produce the results
  * Display the results

---

## Running a Script from a Terminal Command Prompt (1 of 4)

* A way to run a Python script:
  * Open a terminal command prompt window
  * Click in the “Type here to search” box, type Command Prompt, and click Command Prompt in the list
  * Navigate or change directories until the prompt shows directory that contains the Python script
  * Run the script by entering:
    * python3 scriptname.py

---

## Running a Script from a Terminal Command Prompt (2 of 4)

---

## Running a Script from a Terminal Command Prompt (3 of 4)

---

## Running a Script from a Terminal Command Prompt (4 of 4)

* Python installations enable you to launch Python scripts by double-clicking the files from the O S’s file browser
  * May require .py file type to be set
  * Fly-by-window problem: Window will close automatically
    * Solution: Add an input statement at end of script that pauses until the user presses the enter or return key

    ```python
    Input(“Please press enter or return to quit the program. ”)
    ```

---

## Chapter Summary (1 of 3)

* Waterfall model describes software development process in terms of several phases
* Literals are data values that can appear in program
* The string data type is used to represent text for input and output
* Escape characters begin with backslash and represent special characters such as delete key
* A doc string is string enclosed by triple quotation marks and provides program documentation

---

## Chapter Summary (2 of 3)

* Comments are pieces of code not evaluated by the interpreter but can be read by programmers to obtain information about a program
* Variables are names that refer to values
* Some data types: int and float
* Arithmetic operators are used to form arithmetic expressions
  * Operators are ranked in precedence
* Mixed-mode operations involve operands of different numeric data types
* Type conversion functions can be used to convert a value of one type to a value of another type after input

---

## Chapter Summary (3 of 3)

* A function call consists of a function’s name and its arguments or parameters
  * May return a result value to the caller
* Python is a strongly typed language
* A module is a set of resources
  * Can be imported
* A semantic error occurs when the computer cannot perform the requested operation
* A logic error produces incorrect results
