# Getting Started With Python

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Lab Overview

This lab provides an overview of foundational programming syntax in Python, specifically data types/structures, common methods/functions, loops, and operators.

## Acknowledgements

[Click here](https://github.com/kwaldenphd/Python/blob/main/acknowledgements.md) for a full list of acknowledgements for this lab.

# Table of Contents

- [Input & Output](#input--output)
- [Variables & Assignment](#variables--assignment)
- [Basic Data Types](#basic-data-types)
- [Concatenation](#concatenation)
- [Operators](#operators)
- [Other Data Structures](#other-data-structures)
  * [Lists](#lists)
  * [Dictionaries](#dictionaries)
  * [Additional Resources](#additional-resources)
- [Control Flow & Conditional Execution](#control-flow--conditional-execution)
  * [`if-then-else`](#if-then-else)
  * [Loops](#loops)
- [Putting It All Together](#putting-it-all-together)
- [Lab Notebook Questions](#lab-notebook-questions)

[Link to lab procedure as a Jupyter Notebook](https://colab.research.google.com/drive/1QO0I_SYrCF70R6XzHDerOhzHQn4JUoqD?usp=sharing)

# Lab Notebook Template

Lab notebook template:
- [Jupyter Notebook](https://colab.research.google.com/drive/14Zpi8TabYz-AzqbJZkeK14lhD1i_spze?usp=sharing)

# Comments

Comments mark instructions or information in the code that will not run as part of the program. Comments are useful for testing, documenting, and describing what your code is doing. 

In Python, single line comments begin with a pound `#` symbol and multi-line comments are marked by three sets of double quotation marks `"""`.

```Python
# This is an example of a single line comment in Python

"""
This is an example of a multi-line comment in Python
"""
```
 
For more on comments in Python:
- [W3Schools, Python Comments](https://www.w3schools.com/python/python_comments.asp)

#  Variables & Assignment Operators

In most programming languages, variables work as "containers for storing data values" ([W3Schools, Python Variables](https://www.w3schools.com/python/python_variables.asp))

We create a variable by assigning a value to that variable name using an **assignment operator**.

"An assignment statement sets and/or re-sets the value stored in the storage location(s) denoted by a variable name; in other words, it copies a value into the variable...The assignment operator has two operands. The one to the left of the operator is usually an identifier name for a variable. The one to the right of the operator is a value" (Kenneth Leroy Busbee and Dave Braunschweig, "[Assignment](https://press.rebus.community/programmingfundamentals/chapter/assignment/)" in *Programming Fundamentals*)

```
[identifier] [assignment symbol] [value]
```

In Python, the equals sign `=` is the assignment symbol. The underlying syntax for creating a variable in Python using an assignment statement:

```Python
# general syntax
identifier = value

# simple variable example
x = 7

# composite variable example
y = 5 + 7
```

Python has a few restrictions and best practices around variable identifiers or names:

#1- They have to start with a letter character or an underscore (no symbols or numeric characters)

```Python
# example of a valid identifier
x = 7

# example of an invalid identifier
$x = 7
```

#2: Terms that have other meaning or function in Python can't be used as variable identifiers. For example the name of a built-in function (`type`) can't be used as a variable identifier.

Reserved keywords in Python include: `and, except, lambda, with, as, finally, nonlocal, while, assert, fale, None, yield, break, for, not, class, from, or, continue, global, pass, def, if, raise, del, import, return, elif, in, True, else, is, try`

#3: Best practice is any programming language is to use meaningful variable identifiers. Just calling something `x` or `y` won't be particularly helpful to someone else reading or interacting with your code. That said, overly-complex variable identifiers are prone to user error.

We can show the value for a variable using Python's `print()` function.

```Python
# assignment statement
x = 7

# show variable value
print(x)
```

We can also show a variable's data type using the `type()` function.

```Python
# assignment statement
y = "Hello world!"

# show type
print(type(y))
```

<blockquote>Q1: In your own words, explain the difference between the print(hello) command we just used and print(“hello”).</blockquote>

For more background on variables & assignment operators: [Elements of Computing I "Python Intro" lab](https://github.com/kwaldenphd/python-intro)

# Data Types

Commonly-used data types (with Python examples) include:

<table><tr><th>Name</th><th>Python Syntax</th><th>Example</th><th>Description</th></tr>
  <tr><td>String</td><td><code>str()</code><td><code>"Hello World!"</code></td><td>String of characters</td></tr>
  <tr><td>Integer</td><td><code>int()</code><td><code>7</code></td><td>Whole number</td></tr>
  <tr><td>Float</td><td><code>float()</code><td><code>1.5</code></td><td>Decimal number, or number with floating point values</td></tr>
  <tr><td>Boolean</td><td><code>bool()</code><td><code>True</code></td><td>Two-state system that typically represents true/false values</td></tr>
  <tr><td>Nothing/Null/NoneType</td><td><code>NoneType</code><td><code>None</code></td><td>No value</td></tr> 
  </table>
  
For more on data types in Python:
- [W3Schools, Python Data Types](https://www.w3schools.com/python/python_datatypes.asp)

## Numbers

An integer is a whole number that does not include any decimal (or fractional) values. A float data type includes decimal (or fractional) values.

```python
# printing an integer
print(3)

# storing an integer to a variable
number = 3

# show number variable type
print(type(number))

# print number variable
print(number)
```

```Python
# printing a decimal or float value
print(3.5)

# store float value to a variable
number = 3.5

# show number variable type
print(type(number))

# print number variable
print(number)
```

## Strings

A string is a sequence of characters (letters, numbers, symbols, etc.) We can assign strings to a variable (i.e. store them as a variable).

```python
# assign string to variable
s = "Hello world!"

# show variable type
print(type(s))

# print variable
print(s)
```

For more background on basic data types in Python: [Elements of Computing I "Python Intro" lab](https://github.com/kwaldenphd/python-intro#data-types)

# Input & Output (I/O)

In programming languages and computing more broadly, `I/O` stands for `Input` and `Output`. Programming languages can take a variety of inputs (user-provided values, data, files, etc) and return outputs in a variety of formats (data stored in memory, output that shows up in the console, newly-created or -modified files, etc).

We've already seen `I/O` in action in Python via `print()` statements. One way Python accepts input is via the `input()` function, which accepts a user input and assigns that to a variable.

A sample program that asks a user to enter their name:

```Python
# initial prompt
print("Enter your name: ")

# input function
name = input()

# output statement
print("Hello, " + name)
```

We can modify that program to include the initial prompt as part of the `input()` statement.

```Python
# initial prompt with input function
name = input("Enter your name: ")

# output
print("Hello, " + name)
```

NOTE: The default data type for a variable created using the `input()` function is a string object.

For more background on I/O in Python: [Elements of Computing I "Python Intro" lab](https://github.com/kwaldenphd/python-intro#input--output-io)

# Operators

## Arithmetic Operators

Most programming languages allow you to perform arithmetic operations and mathematical calculations using **arithmetic operators**. Common arithmetic operations (with Python examples) include:

<table><tr><th>Name</th><th>Python Syntax</th><th>Python Example</th><th>Description</th></tr>
  <tr><td>Addition</td><td><code>+</code><td><code>5 + 6</code></td><td>Adds values</td></tr>
  <tr><td>Subtraction</td><td><code>-</code><td><code>5 - 6</code></td><td>Subtracts values</td></tr>
  <tr><td>Multiplication</td><td><code>*</code><td><code>5 * 6</code></td><td>Multiples values</td></tr>
  <tr><td>Integer division</td><td><code>//</code><td><code>5 // 6</code></td><td>Divides values, integers (whole numbers)</td></tr> 
  <tr><td>Float division</td><td><code>/</code><td><code>5 / 6</code></td><td>Divides values, floating point numbers (decimal values)</td></tr>
  <tr><td>Modulo</td><td><code>%</code><td><code>5 % 6</code></td><td>Returns or retrieves remainder (whole number) from division operation</td></tr>  
  <tr><td>Exponent</td><td><code>**</code><td><code>5 ** 6</code></td><td>Calculates exponent</td></tr>
  </table>
  
For more on arithmetic operators in Python:
- [W3Schools, Python Arithmetic Operators](https://www.w3schools.com/python/gloss_python_arithmetic_operators.asp)

We can run arithmetic operations directly in the console or in a script.

```Python
# sample arithmetic operation
5 + 7
```

But we can also assign the output of an arithmetic operation to a variable.

```Python
# sample arithmetic operation where output is assigned to variable
x = 5 + 7

# show variable value
print(x)
```

<p align="center"><img src="https://github.com/kwaldenphd/python-intro/blob/main/images/PEDMAS.png?raw=true" width="500"></p>

Python follows the PEDMAS order of operations: parenthesis, exponents, multiplication, division, addition, subtraction. 
- *When in doubt, use parenthesis!*

For more background on arithmetic operators: [Elements of Computing I "Python Intro" lab](https://github.com/kwaldenphd/python-intro#arithmetic-operators)

## Comparison Operators

Relational operators, also called comparison operators, allow us to run `True/False` tests on specific conditions, focusing on the relationship(s) between two or more values.

Relational operators or comparison operators in Python: 

<table><tr><th>Name</th><th>Syntax</th><th>Example</th><th>Description</th></tr>
  <tr><td>Equal</td><td><code>==</code><td><code>x == y</code></td><td>Tests if values are equal</td></tr>
  <tr><td>Not equal</td><td><code>!=</code><td><code>x != y</code></td><td>Tests if values are not equal</td></tr>
  <tr><td>Greater than</td><td><code>></code><td><code>x > y</code></td><td>Tests is a value is greater than another</td></tr>
  <tr><td>Less than</td><td><code><</code><td><code>x < y</code></td><td>Tests is a value is less than another</td></tr> 
  <tr><td>Greater than or equal to</td><td><code>>=</code><td><code>x >= y</code></td><td>Tests if a value is greater than or equal to another</td></tr>
  <tr><td>Less than or equal to</td><td><code><=</code><td><code>x <= y</code></td><td>Tests if a value is less than or equal to another</td></tr>  
  </table>
    
For more on comparison operators in Python: [W3Schools, Python Comparison Operators](https://www.w3schools.com/python/gloss_python_comparison_operators.asp)

- "In mathematics and mathematical logic, Boolean algebra is the branch of algebra in which the values of the variables are the truth values true and false, usually denoted 1 and 0" ([Wikipedia](https://en.wikipedia.org/wiki/Boolean_algebra))

We've talked previously about the Boolean data type. The underlying `True`/`False` logic lets us test for specific conditions and then specify how our code will execute based on the truth value for those conditional statements.

- "You can evaluate any expression in Python, and get one of two answers, `True` or `False`. When you compare two values, the expression is evaluated and Python returns the Boolean answer" ([W3Schools, Python Booleans](https://www.w3schools.com/python/python_booleans.asp))

### Boolean Logic & Comparison Operators
   
We can use comparison operators with a `print()` statement to test whether a particular statement is `True` or `False`.
   
A couple Python examples:

```Python
print(4 == 5) # returns false
print(6 < 10) # returns true
```

```Python
# comparison operator using variables
x = 5
y = 6

print(x > y) # returns false
```

### Comparison Operators & String Objects

We can probably make intuitive sense of how these comparison operators would work for numeric values. But what about text characters or string objects?
   
Most programming languages treat the 26 characters in the English-language alphabet (`a-z`) as sequential values, where `a` is less than `b`, which is less than `c`, etc.

When working with string objects that represent words or characters, comparison operators indicate positionality in the English-language alphabet.

A few examples in Python:
```
print("apple" > "banana") # returns false

print("Ohio State" > "Notre Dame") # returns true
```   

### Logical Operators

We can also compare or relate multiple conditions using logical operators: `and`, `or`, `not`

- "A logical operator is a symbol or word used to connect two or more expressions such that the value of the compound expression produced depends only on that of the original expressions and on the meaning of the operator. Common logical operators include AND, OR, and NOT." (Busbee and Braunschweig, "[Logical Operators](https://press.rebus.community/programmingfundamentals/chapter/logical-operators/)")                           
	  
For example, `5 < 6 and 6 < 7` evaluates whether `5 < 6` and `6 < 7` are true. This statement would return `True`.

Another example: `5 < 6 or 6 > 7` evaluates whether `5 < 6` or `6 > 7` is true. This statement would return `True`.

Logical operators in Python:
    
<table><tr><th>Name</th><th>Syntax</th><th>Example</th><th>Description</th></tr>
  <tr><td>And</td><td><code>and</code><td><code>x == y and y != z</code></td><td>Returns <code>True</code> if both statements are true</td></tr>
  <tr><td>Or</td><td><code>or</code><td><code>x != y or y == z</code></td><td>Returns <code>True</code> if one of the statements is true</td></tr>
  <tr><td>Not</td><td><code>not</code><td><code>not(x == y and y != z)</code></td><td>Reverses the result, returns <code>False</code> if the result is true</td></tr>
  </table>
    
```Python
# example using logical operators
print(5 < 6 and 6 < 7) # returns true because both statements are true

print(5 < 6 or 6 > 7) # returns true because at least one statement is true

print(not(5 < 6 and 6 < 7)) # returns false, inverse of initial true
```

For more background on comparison/relational and logical operators in Python: [Elements of Computing I "Comparison Operators & Conditional Statements" lab](https://github.com/kwaldenphd/python-conditional-statements)

# Data Structures

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Python_Data_Structures.png?raw=true" width="1000"></p>

In addition to what are called "primitive" data types in Python (`integer`, `float`, `string`, and `Boolean`), most programming languages also include or support more complex data structures or more complex ways of storing and accessing information. In Python, those one-dimensional (or linear) data structures include `strings`, `lists`, `tuples`, `sets`, and `dictionaries`.

<table><tr><th>Name</th><th>Syntax</th><th>Example</th><th>Description</th></tr>
  <tr><td>String</td><td><code>str(), ""</code><td><code>"Hello world!"</code></td><td>Sequence of characters</td></tr>
  <tr><td>List</td><td><code>list(), []</code><td><code>["apple", "banana", "pear"], [1, 3, 5, 7]</code></td><td>Sequence of objects/values</td></tr>
  <tr><td>Dictionary</td><td><code>dict(), {}</code><td><code>{'first_name': 'Knute', 'last_name':'Rockne', 'class':'1918'}</code></td><td>Key-value pairs</td></tr>
  <tr><td>Set</td><td><code>set(), {}</code><td><code>{"apple", "banana", "pear"}, {1, 3, 5, 7}</code></td><td>Unordered group of unique values</td></tr> 
  <tr><td>Tuple</td><td><code>tuple(), ()</code><td><code>("apple", "banana", "pear"), (1, 3, 5, 7)</code></td><td>Ordered group of values that can include duplicates</td></tr>
  </table>

## Lists

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/One_Dimensional_Array.jpg?raw=true" width="500"></p>

"In computer science, an array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key...The simplest type of data structure is a linear array, also called one-dimensional array" ([Wikipedia, "Array (data structure)](https://en.wikipedia.org/wiki/Array_(data_structure))")

We can think of arrays as one-dimensional, linear data structures made up of a collection of items. As the definitions note, we can access specific elements in the array by using an index or key value. 

"In Python, the built-in array data structure is a list" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)"). Python also includes a few other built-in array-like data structures, including `sets` and `tuples`. We'll come back to these later in this lab. We can also think of string objects, which are a sequence of characters, as a type of one-dimiensional, linear array.

These **one-dimensional or linear array structures** have a few key properties that differentiate the structures and shape how we can interact with or manipulate them in a programming environment.

Those properties include:
- Mutable: Can values in the structure be changed once it has been created or assigned to a variable?
- Order: Does the order of values in the structure have meaning/significance, or is order not significant?
- Indexing/Slicing: Can values in the structure be accessed using their position or index? Can we isolate values in the structure using their position?
- Duplicates: Does the structure allow duplicate values?

How these properties show up for Python's built-in data structures:

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Python_Array_Comparison.png?raw=true" width="500"></p>

Each structure has its own specific vocabulary and syntax, but some common operations we can use with these structures:
- Getting number of values in the structure (using the `len()` function)
- For structures that are mutable, adding, modifying, and removing values
- Sorting values in the structure
- Testing for membership, if specific value(s) are present in the structure (using the `in` and `not in` operators)
- For structures that are ordered or indexed, accessing elements using their position

An example that uses a list of strings:

```Python
# list of string objects
fruits = ["apple", "banana", "blueberry", "cherry"]

# check data type
print(type(fruits))
```

We can determine the number of elements in the list using the `len()` function.

```Python
print(len(fruits))
```

Remember Python starts at `0` and counts left-to-right. We can access specific values using their position.

```Python
# access first value 
print(fruits[0])

# access second value
print(fruits[1])

# access third value
print(fruits[2])
```

Python lists also support negative indexing- we can use negative index values to count right-to-left. 
- NOTE: Negative indexing starts counting at `-1`

```Python
# access last value
print(fruits[-1])

# access next to last value
print(fruits[-2])
```

## Dictionaries

<p align="center"><img src="https://github.com/kwaldenphd/python-data-structures/blob/main/images/Associative_Arrays.png?raw=true" width="500"></p>

The other primary type of array we can encounter is an **associative array**, "an abstract data type that stores a collection of (key, value) pairs, such that each possible key appears at most once in the collection" ([Wikpedia, Associative Array](https://en.wikipedia.org/wiki/Associative_array))

Python stores associate arrays using the **dictionary** data structure. Python dictionaries consist of key-value pairs, where the key is working as an identifier or index.

A preliminary example in Python:

```Python
# create dictionary
english_to_french = {
  'one': 'un',
  'two': 'deux',
  'three': 'trois',
  'four': 'quatre',
  'five': 'cinq'
}

# check data type
print(type(english_to_french))
```

We can use the index operator (`[]`) and key values to select specific values in the dictionary.

```Python
# access value for one key
print(english_to_french['one'])

# access value for five key
print(english_to_french['five'])

# access value for asdf key
print(english_to_french['asdf'])
```

The last line will return a `KeyError` because `asdf` is not a key in this dictionary.

For more background on arrays and data structures in Python: [Elements of Computing I "Data Structures in Python" lab](https://github.com/kwaldenphd/python-data-structures)

# Conditional Statements & Control Flow

## `if-then-else`

From Busbee and Braunschweig's "[Selection Control Structures](https://press.rebus.community/programmingfundamentals/chapter/selection-control-structures/)" from *Programming Fundamentals*:
- "The basic attribute of a selection control structure is to be able to select between two or more alternate paths. This is described as either two-way selection or multi-way selection. A question using Boolean concepts usually controls which path is selected. All of the paths from a selection control structure join back up at the end of the control structure, before moving on to the next lines of code in a program."
- "The if then else control structure is a two-way selection"

In Python, this logic is expressed using the `if`, `else`, and `elif` syntax. From W3Schols, "[Python Conditions](https://www.w3schools.com/python/python_conditions.asp)":
- "An 'if statement' is written by using the `if` keyword"
- "The `elif` keyword is Python's way of saying 'if the previous conditions were not true, then try this condition'"
- "The `else` keyword catches anything which isn't caught by the preceding conditions"

```Python
# assign variables
x = 5
y = 7

# if statement
if x > y:
    print("The value of x is greater than the value of y")

# else if statement
elif x == y:
    print("The value of x is equal to the value of y")

# else statement
else:
    print("The value of x is less than the value of y")
```

To frame this another way:
- `if` introduces and evaluates an initial condition. The lines of code indented under `if` will only run when the `if` statement is `True`
- `else-if` or `elif` introduces and evaluates another condition. The lines of code indented under `elif` will only run when the `elif` statement is `True`
- `else` **does not** introduce a new condition. The lines of code indented under `else` will only run when the preceeding `if`/`elif` statements **are not** true 

For more background on `if-then-else` logic in Python: [Elements of Computing I "Comparison Operators & Conditional Statements" lab](https://github.com/kwaldenphd/python-conditional-statements)

## Iteration

But let's review the definition of iteration as a control structure. From Busbee and Braunschweig's "[Iteration Control Structures](https://press.rebus.community/programmingfundamentals/chapter/iteration-control-structures/)," in *Programming Fundamentals*:

"In iteration control structures, a statement or block is executed until the program reaches a certain state, or operations have been applied to every element of a collection. This is usually expressed with keywords such as `while`, `repeat`, `for`, or `do..until`. The basic attribute of an iteration control structure is to be able to repeat some lines of code. The visual display of iteration creates a circular loop pattern when flowcharted, thus the word 'loop' is associated with iteration control structures."

Breaking down that definition:
- Iteration (repetition of a process) is a type of control structure
- In programming languages, iteration involves lines of code repeating until a condition is met of the end of a group of values has been reached.
- Because iteration in this context involves a circular pattern, many object-oriented programming languages refer to these structures as `loops`

The power of iteration as a control structure comes from a programming concept called `loops`.

<p align="center"><img src="https://github.com/kwaldenphd/python-loops-iteration/blob/main/images/loop-comparison-diagram.png?raw=true" width="1000"></p>

Most high-level programming languages support two main types of loops: event-controlled and count-controlled
- **Event-controlled loops** test for an initial condition, and execution continues as long as the initial condition is `True`. How many times the loop will execute *is not known*.
- **Count-controlled loops** (sometimes called counter-controlled loops) continue executing for a pre-determined number of times. The number of times the loop will execute is known because the loop is iterating through a collection of objects/values (i.e. a string or list), or the iteration when the initial condition will no longer be `True` is known.

### `while`

<p align="center"><img src="https://github.com/kwaldenphd/python-loops-iteration/blob/main/images/while-loop-diagram.png?raw=true" width="500"></p>

In Python, event-controlled loops are written using a `while` statement and are called `while loop`. A `while` statement tests for an initial condition, and the lines of code indented under `while` run only when the initial condition is `True`.

In each iteration through the `while` loop, Python will:
- Evaluate the initial condition (which is a Boolean true/false expression)
- If the condition is `False`, exit the loop and continue the program
- If the condition is `True`, then execute other statements in the body of the loop and return to the beginning of the loop

The basic syntax for a `while` loop:

```Python
# while loop sample syntax
while condition:
	statement(s)
```

To express this logic another way:

```Python
# while loop sample syntax
while THIS CONDITION IS TRUE:
	DO THIS THING
```

For example, let's look at a guessing game program that uses a `while` statement:

```Python
# correct answer
secret = 7

# guess
guess = int(input("Guess a number: "))

# while statement
while guess != secret:
  if guess > secret:
    print("Your guess is too high. Better luck next time")
    guess = int(input("Guess again. Enter another number: "))
  else:
    print("Your guess is too low. Better luck next time.")
    guess = int(input("Guess again. Enter another number: "))
  

print("Congrats, you guessed the secret number!")
```

This is an example of a `while` loop. Because the number of times the loop will execute is not known, this is an example of an event-controlled loop. That is, the loop will continue executing (looping) until the initial condition (`guess != secret`) is no longer true.

### `for`

<p align="center"><img src="https://github.com/kwaldenphd/python-loops-iteration/blob/main/images/for-loop-diagram.png?raw=true" width="500"></p>

In Python, count-controlled loops are written using a `for` statement and are called `for loop`. A `for loop` iterates over each value in a group of values- the lines of code nested under the initial statement run for each iteration.

`for` loops let us iterate through a definite set of objects. In each iteration through the `for` loop, Python will:
- Extract one element from the dataset
- Execute the body of the `for` loop using the item bound to the element
- Go back to the first step
- Keep iterating through the loop until reaching the end of the dataset

The basic syntax in a `for` loop:

```Python
# sample for loop syntax
for item in dataset:
 statement(s)
```

In this syntax, `item` is a placeholder for each element in `dataset`. We can replace `item` with another word or letter character.

```Python
# sample for loop syntax
for i in dataset:
	statement(s)
```

In this syntax, `dataset` stands for the group of items we want Python to iterate over. That group of items could be a list, a list variable, string, string variable, etc. 

Let's say we have a list of numbers, and we want Python to iterate through each number in the list and print the number.

```Python
for i in [0, 1, 2, 3]:
 print(i)
```

Alternatively, we could create a variable for our list of numbers.

```Python
# create list of numbers
number_list = [0, 1, 2, 3]

# for loop
for i in number_list:
 print(i)
```

The loop command steps through the list one value at a time. The loop continues until it reaches the end of the list. 

We can also use a `for` loop to iterate over a list of strings. Let's say we have a list of pepper types.

```Python
peppers = ["bell", "poblano", "jalapeno", “banana”, “chile”, “cayenne”]
```

We can use a `for` loop to iterate over each string in the list.

```Python
peppers = ["bell", "poblano", "jalapeno", “banana”, “chile”, “cayenne”]

for x in peppers:
 print(x)
```

We can also use a `for` loop to iterate through characters in a single string. Let's say we want to iterate over the characters in the string `elements`.

```Python
for x in 'elements':
 print(x)
```

```Python
# another example of iterating over characters in a string

string = 'elements'

for x in string:
 print(x)
```

For more background on iteration & loops in Python: [Elements of Computing I "Iteration & Loops" lab](https://github.com/kwaldenphd/python-loops-iteration)

<blockquote>Q3: In your own words, what is iteration?</blockquote>

<blockquote>Q4: In your own words, what is the difference between a `for` loop and a `while` loop?</blockquote>

# Putting it all together

Q5A: The last thing we'll do in this lab is make sure you're comfortable with a few core elements of Python syntax. For each component, you're asked to describe the concept in your own words and write an example of the concept using Python syntax.

Q5B: These examples do not need to be overly complex.
  * Modifying example code provided in the lab is absolutely fine. 
  * Using things you wrote while working through the lab is absolutely fine. 
  * Consulting linked resources is fine (include a comment or note that mentions any resources you consulted beyond the lab procedure.

Q5C: For each concept, describe in your own words and provide an example using Python syntax. Use comments/narrative text to note each part of your answer.
- `I/O` (input and ouput, using `print()` and `input()`)
- string variable
- integer variable
- concatenation
- arithmetic operators
- comparison operators
- dictionary
- `if, else, elif` statements
- `for` loop
- `while` loop

# Lab Notebook Questions

Q1: In your own words, explain the difference between the `print(hello)` command and `print(“hello”)`.

Q2: Create your own list of numbers or strings, using the examples in the lab as a starting point. What is the number position for each of the items in your list? How would you return the value of the first item? How would you return the value of the last item?

Q3: In your own words, what is iteration?

Q4: In your own words, what is the difference between a `for` loop and a `while` loop?

Q5: For each concept, describe in your own words and provide an example using Python syntax. Use comments/narrative text to note each part of your answer.
- `I/O` (input and ouput, using `print()` and `input()`)
- string variable
- integer variable
- concatenation
- arithmetic operators
- comparison operators
- dictionary
- `if, else, elif` statements
- `for` loop
- `while` loop
