# Getting Started With Python

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Lab Overview

This lab provides an overview of foundational programming syntax in Python, specifically data types/structures, common methods/functions, loops, and operators.

## Acknowledgements

[Click here](https://github.com/kwaldenphd/Python/blob/master/acknowledgements.md) for a full list of acknowledgements for this lab.

# Table of Contents

- [`print` statements](#print-statements)
- [Variables](#variables)
- [Data Types](#data-types)
  * [Comments](#comments)
  * [Numbers](#numbers)
  * [Strings](#strings)
- [Concatenation](#concatenation)
- [Operators](#operators)
  * [Arithmetic Operators](#arithmetic-operators)
  * [Comparison Operators](#comparison-operators)
  * [Logical Operators](#logical-operators)
  * [Additional Resources](#additional-resources)
- [Lists](#lists)
- [Dictionaries](#dictionaries)
- [`if, else, elif` statements](#if-else-elif-statements)
- [Loops](#loops)
  * [`for` loops](#for-loops)
  * [`while` loops](#while-loops)
- [Putting It All Together](#putting-it-all-together)
- [Lab Notebook Questions](#lab-notebook-questions)

[Link to lab procedure as a Jupyter Notebook](https://colab.research.google.com/drive/1QO0I_SYrCF70R6XzHDerOhzHQn4JUoqD?usp=sharing)

# Lab Notebook Template

Lab notebook template:
- [Jupyter Notebook](https://colab.research.google.com/drive/14Zpi8TabYz-AzqbJZkeK14lhD1i_spze?usp=sharing)

# `print` statements

For each of these examples, copy/paste or retype the code to run each mini program (and learn more about Python's functionality and documentation). Experiment, adapt, or modify these samples as you work through the lab procedure.

1. Your first program will contain a single Python statement. Enter the following statement into a code cell.

<blockquote>Watch out for quotation marks!</blockquote>

```python
print ("Welcome to the wild world of computer programming!")
```

2. Run the code cell to see the `print()` statement output.

3. The `print()` function will output the value passed to it, in this case a string of characters (letters).

4. You can modify the characters or symbols in the quotation marks to print other values.

# Variables

5. Next, we're going to assign our first variable.

6. In Python, a variable is a placeholder for a piece of information. 

```Python
# assign "hello world" message to hello variable
hello = "Hello World"

# print hello variable
print(hello)
```

7. Run this program to see the `print()` statement output.

8. In this example, the `"Hello World"` string of characters is assigned to a variable named `hello`.

9. You can choose variable names, as long as they meet a few conditions...
  * Don't include spaces
  * No special characters
  * Don't begin with a number
  * Aren't words that are also commands in Python (for example, `print` is an instruction and can't be a variable name)
  
10. For more on variables in Python: https://www.w3schools.com/python/python_variables.asp
  
<blockquote>Q1: In your own words, explain the difference between the print(hello) command we just used and print(“hello”).</blockquote>

# Data Types

11. Python includes a number of different data types, which can be stored as variables.

12. We'll do more with variables later, but for now...

## Comments

13. We can add comments to our code to include information about what is happening in the program.

14. In Python, lines that are comments begin with the `#` symbol.

15. Going back to a previous `print()` statement example:

```Python
# assign "hello world" message to hello variable
hello = "Hello World"

# print hello variable
print(hello)
```

16. We see comments in action- lines that begin with `#` that are part of the program but not instructions or commands.

17. To put that another way, comments are for human users, not the machine.

18. For more on comments in Python: https://www.w3schools.com/python/python_comments.asp

## Numbers

19. An integer is a whole number that does not include any decimal (or fractional) values. A float data type includes decimal (or fractional) values.

```python
# printing an integer
print(3)

# storing an integer to a variable
number = 3

# show number variable type
type(number)

# print number variable
print(number)
```

```Python
# printing a decimal or float value
print(3.5)

# store float value to a variable
number = 3.5

# show number variable type
type(number)

# print number variable
print(number)
```

<blockquote>It may seem odd at first, but in Python, the "equals sign" here does not denote equality. Rather, it is an instruction telling Python to assign the value on its right into the variable on its left.</blockquote>

20. For more on numbers in Python: https://www.w3schools.com/python/python_numbers.asp

## Strings

21. A string is a sequence of characters (letters, numbers, symbols, etc.)

22. We can assign strings to a variable, or store them as a variable.

```python
# assign string to variable
s = "Hello world!"

# show variable type
type(s)

# print variable
print(s)
```

23. For more on strings in Python: https://www.w3schools.com/python/python_strings.asp

# Concatenation

24. In Python, we can add or join strings using a concept called concatenation.

25. Specifically we can use the `+` symbol to connect two strings.

26. Let's look at an example using first and last names:

```Python
# assign first name to variable
firstName = "Katherine"

# assign last name to variable
lastName = "Walden"

# use concatenation to create full name
print(firstName + lastName)
```

27. We notice the last program's output doesn't include a space between first and last name.

28. We can address this issue using...concatenation.

```Python
# assign first name to variable
firstName = "Katherine"

# assign last name to variable
lastName = "Walden"

# use concatenation to create full name with space between strings
print(firstName + " " + lastName)
```

29. We could also use concatenation to create a new `fullName` variable.

```Python
# assign first name to variable
firstName = "Katherine"

# assign last name to variable
lastName = "Walden"

# use concatenation to create full name and assign to variable
fullName = firstName + " " + lastName

# pring fullName variable
print(fullName)
```

30. For more on concatenation: https://www.w3schools.com/python/python_strings_concatenate.asp

# Operators

31. Python includes a few different types of operators that can be used with values and variables.

<table>
 <tr><td>Operator Type</td>
 <td>Example</td>
 <td>Description</td>
 </tr>
 <tr><td>Arithmetic operators</td>
 <td><code>+, -, *, /</code></td>
 <td>Used to perform arithmetic operations or calculations</td>
 </tr>
 <tr><td>Assignment operators</td>
 <td><code>=</code></td>
 <td>Used to assign values to variables</td>
 </tr>
 <tr><td>Comparison operators</td>
 <td><code>==, !=, >, <</code></td>
 <td>Used to compare two values</td>
 </tr>
 <tr><td>Logical operators</td>
 <td><code>and, or, not</code></td>
 <td>Used to combine conditional statements</td>
 </tr>
</table>

## Arithmetic Operators

32. A few standard operators we can use in Python to perform arithmetic operations.
- `+` (plus, sum)
- `-` (minus, subtraction)
- `*` (times, multiplication)
- `//` (divide, integer division)
- `/` (divide, float division)
- `%` (modulo operator, used to return/retrieve remainder after division)
- `**` (exponent)

33. Python follows the PEDMAS order of operations. When in doubt, use parenthesis!

<blockquote>PEDMAS order of operations: parenthesis, exponents, multiplication, division, addition, subtraction</blockquote>

```Python
# a few examples of arithmetic operators in action
print(2+3)
print(2-3)
print(2*3)
print(2/3)
```

## Comparison Operators

34. Python's comparison operators will return a value of `TRUE` or `FALSE` based on whether the comparison is true or false.

<table>
 <tr><td>Operator</td>
 <td>Name</td>
 <td>Example</td>
 </tr>
 <tr><td><code>==</code></td>
 <td>Equal</td>
 <td><code>x == y</code></td>
 </tr>
 <tr><td><code>!=</code></td>
 <td>Not equal</td>
 <td><code>x != y</code></td>
 </tr>
 <tr><td><code>></code></td>
 <td>Greater than</td>
 <td><code>x > y</code</td>
  </tr>
  <tr><td><code><</code></td>
   <td>Less than</td>
   <td><code>x < y</code</td>
  </tr>
  <tr><td><code>>=</code></td>
   <td>Greater than or equal to</td>
   <td><code>x >= y</code></td>
  </tr>
  <tr><td><code><=</code></td>
   <td>Less than or equal to</td>
   <td><code>x <= y</code></td>
  </tr>
  </table>
  
35. These comparison operators compare two values and return `True` or `False`.

36. A few examples of comparison operators in Python:

```python
# assign integer to variable
x=4

# show operator type
print(type(x == 4))

# output true/false based on comparison statement
print(x==4)
```

```python
# in some cases, operators can be chained or combined

# will output true because comparison is true
print(1 < 2 < 3)

# will output false because comparison is false
print(10 < 2 < 3)
```

```python
# assigning integer values to variables
x = 3
y = 18
z = 10

# comparing variables (will return true/false based on whether the comparison is true)
print (x < y < z)
```

37. For more on comparison operators in Python: https://www.w3schools.com/python/gloss_python_comparison_operators.asp

## Logical Operators

38. We can also combine comparison operators using Python's logical operators.

<table>
 <tr><td>Operator</td>
 <td>Description</td>
 <td>Example</td>
 </tr>
 <tr><td><code>and</code></td>
 <td>Returns <code>True</code> if both statements are true</td>
 <td><code> x < 5 and x < 10</code></td>
 </tr>
 <tr><td><code>or</code></td>
 <td>Returns <code>True</code> if one of the statements is true</td>
 <td><code>x < 5 or x < 4</code></td>
 </tr>
 <tr><td><code>not</code></td>
 <td>Reverses the result; returns <code>False</code> if the result is <code>True</code></td>
 <td><code>not(x < 5 and X < 10)</code></td>
 </tr>
 </table

## Additional Resources

39. To learn more about operators in Python:
  * [Arithmetic operators](https://www.w3schools.com/python/gloss_python_arithmetic_operators.asp)
  * [Comparison operators](https://www.w3schools.com/python/gloss_python_comparison_operators.asp)
  * [Logical operators](https://www.w3schools.com/python/python_operators.asp)

# Lists

40. Python allows us to store information in a few different ways. 

41. Let’s start with lists. 
  * Lists are an ordered collection of items
  * They can be numbers or strings. 
  * The individual values in a list are called elements or items
  * Lists are typically assigned to a variable
  * Items in a list are contained within `[ ]` and the individual items are separated by a comma (`,`). 

## Lists of Strings

42. Write a list of a few of your favorite things.

```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
```

43. We can print this list with a print function `print(cookies)`, but Python returns a representation of the list, just as we entered it.
`['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']`

44. This isn’t particularly useful by itself; however, we can use the position of each item (called the *index*) to perform different functions.

45. Add a print function calling a specific item on your list.
```Python
print(cookies[0])
```

46. This command returns the first item on my list. This is the item in the `0` position on my list.

```Python
chocolate chip
```

47. Items in a list are indexed with a number, **beginning with 0 NOT 1.**

48. A `print` command that outputs the last item on my list of four items would look like this.
```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
print(cookies[3])
```

49. We can also work backwards on our list using negative numbers. For example, to call the last item on the list we could also use the index value `-1`.

```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
print(cookies[-1])
```

50. To return the second to last item, we could use -2. For the third to last -3, etc. etc.

51. We can concatenate our list items in strings.

```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
print("My favorite cookie to bake is " + cookies[1] + ".")
```

52. Which outputs `My favorite cookie to bake is snickerdoodle.`

53. We can  use `append` to add values to a list

```Python
# create empty list and assign to variable
myPets = []

# add one string to list
myPets.append('Christy Matthewson')

# add another string to list
myPets.append('Smoky Jo Wood')

# add a third string to list
myPets.append('Sandy Koufax')

# show list
print(my_pets)
```

54. In this block of code, we started with an empty list `[]`. Then the next lines with `append` added new items to the list.

## Lists of Numbers

55. We can also create a list of numbers in Python

```Python
# create list with numbers and assign to variable
num_list = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377]

# show first number in list
num_list[0]

# show last number in list
num_list[-1]

# show full list
num_list
```

<blockquote>Q2: Create your own list of numbers or strings, using the examples in the lab as a starting point. What is the number position for each of the items in your list? How would you return the value of the first item? How would you return the value of the last item?</blockquote>

# Dictionaries

<p align="center"><a href="https://github.com/kwaldenphd/python-dictionaries-sets/blob/master/figures/Dic_1.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/python-dictionaries-sets/blob/master/figures/Dic_1.png?raw=true" /></a></p>

<p align="center"><a href="https://github.com/kwaldenphd/python-dictionaries-sets/blob/master/figures/Dic_2.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/python-dictionaries-sets/blob/master/figures/Dic_2.png?raw=true" /></a></p>

56. A dictionary is a mapping between a set of indices (keys) and a set of values. 

57. Each key maps to a value. 

58.  The association of a key and a value is called a key-value pair.

## Creating a Dictionary

59. We have two options for creating a dictionary.

60. We can use the `dict()` function or the `{}` syntax.

61. Examples for each:

```Python
# creating empty dictionary using dict()
english_to_french = dict({})

# check variable type
type(english_to_french)

# create dictionary this time with key-value pairs
english_to_french = dict({
  'one': 'un',
  'two': 'deux',
  'three': 'trois',
  'four': 'quatre',
  'five': 'cinq'
})
```

```Python
# create empty dictionary using curly brackets {}
english_to_french = {}

# check variable type
type(english_to_french)

# create dictionary this time with key-value pairs
english_to_french = {
  'one': 'un',
  'two': 'deux',
  'three': 'trois',
  'four': 'quatre',
  'five': 'cinq'
}
```

## Interacting With A Dictionary

62. Now that we have a dictionary, we can start to interact with values in the dictionary.

```Python
print(english_to_french)
```

63. Notice that when we print the dictionary, the key-value pairs are **unsorted** and do not appear in the order in which we added them.

64. Due to the nature of the dictionary data structure, we cannot make any assumptions about the order in which items appear in the dictionary.

65. We can use the index operator to read the value for a particular key.

```Python
# access value for 'one' key
english_to_french['one']
```

66. If we try to access the value for a key that does not exist, Python will return a KeyError.

```Python
english_to_french['asdf']
```

67. We can use the `.keys()` method to get a list of all keys in the dictionary.

```Python
print(english_to_french.keys())
```

68. We can use the `.values()` method to get a list of all the values in the dictionary.

```Python
print(english_to_french.values())
```

69. For more on Python dictionaries: https://www.w3schools.com/python/python_dictionaries.asp

# `if, else, elif` statements

70. We can use conditional statements to change the behavior of a program based on whether specific conditions are or are not met.

71. To put this another way, conditional statements check boolean expressions (i.e. conditions), and change the behavior of the program accordingly.

## Operator Review

72. Operators used to compare two objects:
- `==`    equal to
- `==`    equal to
- `!=`    not equal to
- `>=`    greater than or equal to
- `>`     greater than
- `<`     less than
- `<=`    less than or equal to

73. Boolean logical operators:
- `and`   both must be true
- `or`    one or both must be true
- `not`   reverses the truth value

74. We can use and test for conditions in a few key ways, specifically through `if` statements and `loops`.

75. More on loops later, but for now...

76. Python's comparison operators serve as conditional tests that return a True or False.

```Python
# set the variable number to 10
number = 10

# the following statements will return true or false

# EQUAL !==
print(number == 15)
print(number ==10)

# GREATER THAN >
print(number > 10)
print(number > 4)

# LESS THAN <
print(number < 10)
print(number < 15)

# GREATER THAN OR EQUAL TO >=
print(number >= 15)
print(number >= 10)

# LESS THAN OR EQUAL TO <=
print(number <= 4)
print(number <= 10)

#TESTING MULTIPLE CONDITIONS

#AND
print(number > 1 and number <20)

#OR
print(number ==10 or number ==20)
```

## `if` Statements

77. `if` statements use the `if` keyword to test if a condition is true.

78. `if` statements are conditional, meaning that there is a test to determine if a statement is true or false, and then the computer takes some defined action.

79. The basic syntax for an `if` statement:

```Python
if condition:
 statement(s)
```

80. The `if` statement tests if a particular condition is true. And if so, executes the command nested under the initial `if` statement.

81. To illustrate that another way:

```Python
if this condition is true:
 then do this thing
```

82. A couple things to note about this syntax:
- A colon always follows the first line of an `if` statement
- The code that will run if the statement is true is nested or intented beneath the `if` keyword

83. For example, let's say we have a Python program where the variable `n` equals `0`.

84. We want to write a program that, if `n` equals `0`, prints the message `n is zero`.

85. We can do that using an `if` statement.

```Python
n = 0

if n == 0:
 print('n is zero')
```

## `if-else` Statements

86. Suppose we want to print one message when the condition (`number > 0`) is true, and a different message when the condition is false. 

87. We can do that by using an `else` clause along with an `if` keyword.

88. The basic syntax for `if-else`:

```Python
if condition:
 statement(s)
else:
 statement(s)
```

89. The statement indented beneath the `if` keyword will only run when the `if` condition is true.

90. In an `if-else` statement, the statement indented beneath `else` will only run if the `if` condition is not true (or false).

91. An example that illustrates this logic:

```Python
# ask user to enter a number
number = input("Enter a number: ")

# test if number is greater than zero
if number > 0:
  print ("That number is positive.")

# if number is not greater than zero
else:
  print ("Definitely NOT positive.")

# message that prints at end of program
print ("This message prints every time.")
```

## `elif` statements

92. We can also use the `elif` keyword along with the `if` keyword to introduce a new condition. 

93. Python will test the `elif` condition if previous conditions are not true.

```Python
# elif statement example

# declares x variable
x = 1

# block of code that runs if x is less than 0
if x < 0:
 print("x is less than 0")

# block of code that runs if x equals zero
elif x == 0:
 print("x is equal to 0")

# block of code that runs if x is greater than 0
else:
 print("x is greater than 0")
```

```Python
# another elif example

# assign a variable 
a = 33

# assign b variable 
b = 33

# conditional statement using if
if b > 1:
 print("b is greater than a")
 
# conditional statment using elif to test, only when if statement is false
elif a == b:
 print("a and b are equal")
```

94. For more information on `if, else, elif`: https://www.w3schools.com/python/python_conditions.asp

# Loops

95. Loop statements are a type of conditional statement that rely on the underlying logic of conditional execution.

96. In Python, loops repeatedly execute a series of tasks.
- Key term: *loop(s), looping*

97. Each time through the body of a loop is called an iteration.
- Key term: *iteration*

98. An iteration can involve things like iterating through items in a list or testing if specific conditions are met, and then doing “something” as the result or endpoint for the loop.

## `for` Loops

99. `for` loops let us iterate through a definite set of objects.

100. In each iteration through the `for` loop, Python will:
- Extract one element from the dataset
- Execute the body of the `for` loop using the item bound to the element
- Go back to the first step
- Keep iterating through the loop until reaching the end of the dataset

101. The basic syntax in a `for` loop:

```Python
for item in dataset:
 statement(s)
```

102. In this syntax, `item` is a placeholder for each element in `dataset`. 

103. You can replace `item` with another word or letter character.

```Python
for i in dataset
```

104. In this syntax, `dataset` stands for the list of items we want Python to iterate over.

105. That list of items could be a list variable, a list of numbers, a string of characters, etc.

### `for` Loops and Lists of Numbers

106. Let's say we have a list of numbers, and we want Python to iterate through each number in the list and print the number.

```Python
for i in [0, 1, 2, 3]:
 print(i)
```

107. Alternatively, we could create a variable for our list of numbers.

```Python
# create list of numbers
number_list = [0, 1, 2, 3]

# for loop
for i in number_list:
 print(i)
```

108. The loop command steps through the list one value at a time. 

109. The loop continues until it reaches the end of the list. 

### `for` Loops and Strings

110. We can also use a `for` loop to iterate over a list of strings.

111. Let's say we have a list of pepper types.

```Python
peppers = ["bell", "poblano", "jalapeno", “banana”, “chile”, “cayenne”]
```

112. We can use a `for` loop to iterate over each string in the list.

```Python
peppers = ["bell", "poblano", "jalapeno", “banana”, “chile”, “cayenne”]

for x in peppers:
 print(x)
```

113. We can also use a `for` loop to iterate through characters in a single string.

114. Let's say we want to iterate over the characters in the string `elements`.

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

115. Let's start combining `for` loops with some the other concepts we've covered.

```Python
#loops through a list of the members of the House Stark.

characters = ['Arya', ' Benjen', 'Bran', 'Catelyn', 'Eddard', 'Rickon', 'Robb', 'Sansa']

for character in characters:
  print(character.title() + "Stark")
```

<blockquote>Note the use of the plural for the name of the list and the singular for the individual item is not required. We are just declaring variables here. We can use anything to name the individual items (e.g. for person in characters). All this does is set a new variable for the individual item. Standard convention is to use the plural and singular terms so that the person reading the code can interpret what it is doing.</blockquote>

116. Remember the loop command steps through the list one value at a time. The loop continues until it reaches the end of the list. 

117. In this case, for each item in the list called `“characters”` the program prints the value of each `“character”` in the list concatenated with the string `" Stark”`. 

118. This produces the output:
```
Arya Stark
Benjen Stark
Bran Stark
Catelyn Stark
Eddard Stark
Rickon Stark
Robb Stark
Sansa Stark
```

119. For more information on `for` loops: https://www.w3schools.com/python/python_for_loops.asp

## `while` Loops

120. Another way to modify the control flow of a program is to have it execute one or more statements repeatedly.

121. A `while` loop will test for an initial condition and continue iterating through the loop until the condition is `False`.

122. In each iteration through the `while` loop, Python will:
- Evaluate the initial condition (which is a Boolean true/false expression)
- If the condition is `False`, exit the loop and continue the program
- If the condition is `True`, then execute other statements in the body of the loop and return to the beginning of the loop

123. The basic syntax for a `while` loop:

```Python
while condition:
 statement(s)
```

124. To express this logic another way:

```Python
while THIS CONDITION IS TRUE
 DO THIS THING
```

### `while` Loop Examples

#### `while` Loop Example A

125. Let's look at a sample `while` loop that uses the `<` (less than) comparison operator.

```Python
n = 0

while n < 10:
 print(n)
 n = n +1
```

126. To walk through what is happening in each line of this program...

127. `n=0` assigns the value zero (0) to the variable `n`.

128. `n < 10` is a conditional statement that will return `True` as long as `n` is less than `10`.

129. So `while n < 10` sets up a `while` loop in which the body of the loop (the lines of code nested or indented beneath the first line of the loop) will run as long as the initial condition is `true`.

130. The first line in the body of the loop `print(n)` prints the value of `n` for that iteration.

131. The second line in the body of the loop `n = n+1` reassigns the value of `n` to be `n + 1`.

132. After executing both lines in the body of the loop, the next iteration of the loop begins by evaluating the `n < 10` conditional statement.

#### `while` Loop Example B

133. Another example of a `while` loop.

```Python
# assign x variable
x = 10

# looping structure using greater than or equal to conditional statement
while x >= 0:
 print(x)
 x = x-1

# message to print once loop has completed
print("I'm done!")
```

134. For more information on `while` loops: https://www.w3schools.com/python/python_while_loops.asp

<blockquote>Q3: In your own words, what is iteration?</blockquote>

<blockquote>Q4: In your own words, what is the difference between a `for` loop and a `while` loop?</blockquote>

# Putting it all together

135. The last thing we'll do in this lab is make sure you're comfortable with a few core elements of Python syntax.

136. For each component, you're asked to describe the concept in your own words and write an example of the concept using Python syntax.

137. These examples do not need to be overly complex.
  * Modifying example code provided in the lab is absolutely fine. 
  * Using things you wrote while working through the lab is absolutely fine. 
  * Consulting linked resources is fine (include a comment or note that mentions any resources you consulted beyond the lab procedure.

Q5: For each concept, describe in your own words and provide an example using Python syntax. Use comments/narrative text to note each part of your answer.
- `print()` statement
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
- `print()` statement
- string variable
- integer variable
- concatenation
- arithmetic operators
- comparison operators
- dictionary
- `if, else, elif` statements
- `for` loop
- `while` loop
