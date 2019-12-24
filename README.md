# Introduction to Python

## Lab Objectives

By the end of this project you will be able to:
-	Describe the differences between a high-level programming language and machine language
-	Use Geany to write and execute Python programs
-	Use Python methods and functions to work with strings and numbers
-	Assign variables, concatenate strings, create lists, and define dictionaries
-	Use Python to parse XML using the ElementTree Module

Python is an object-oriented programming language. It’s comparable to a number of other programming languages, such as Perl, Ruby, or Java. Python is a high- level programming language.

## Object-Oriented Programming

Object-oriented programming languages allow programmers to write sections of re-usable code, including object definitions and function definitions. Objects describe some object or concept from the real-world in code form. Functions then define the way that objects interact or how they function.

## High-Level Programming Languages

<p align="center"><a href="https://github.com/kwaldenphd/Python/blob/master/images/Image_1.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/Python/blob/master/images/Image_1.png?raw=true" /></a></p>

High-level programming languages refer to programming languages that resemble human languages. High-level languages are abstractions of low-level languages like binary (a machine language). Assembly languages are an intermediary. A complier translates the high-level language into an assembly language, and an assembler translates the assembly language into the machine language.

Remember, we used the machine language (aka binary code) in a previous lab.

We are going to look a just a few basics that are common to all programming languages. While syntax will differ slightly from language to language, these basic functions can be performed in all languages.

# Task 1: Hello World

Your Pi comes installed with a Python programming environment, but we’ll stick with Geany for this lab. We'll write our first Python program using a variation on the now familiar “Hello World!”

Open a new file in Geany and save it as Hello_World.py. The .py extension on the file name tells Geany that we are writing Python (rather than .html or .xml).

```Python
print("Hello World!")
```
Type the code listed above.

<p align="center"><a href="https://github.com/kwaldenphd/Python/blob/master/images/Image_3.jpg?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/Python/blob/master/images/Image_3.jpg?raw=true" /></a></p>

Notice that as with our other HTML and XML projects, Geany has highlighted the syntax for us to make debugging easier.

Now we need to run the file – either press F5 or select Build > Execute from the menu. A terminal window should open with the phrase “Hello World!”

You have just successfully written your first Python program. What just happened? 

When you select Execute from the menu, Geany runs the file through the Python interpreter, this is another program that reads though the Python code that you just wrote and determines what each piece of code means and then executes the code (or runs it). 

In this example, the Python interpreter recognizes the word print as a Python function. This function allows you to “print” to the screen or send output to the computer screen. 

The brackets () contain the information to be printed. In this case you have entered a string “Hello World.” 

<blockquote>A string is any series of characters. Strings are identified by the <code>“ ”</code> or alternatively by <code>‘ ’</code>.</blockquote>

Let’s change this program a bit. We are going to assign our first variable. A variable is a placeholder for a piece of information. You can think of it as a basket or container. 

Let’s modify the code as follows:

```Python
hello="Hello World"
print(hello)
```
<p align="center"><a href="https://github.com/kwaldenphd/Python/blob/master/images/Image_3.jpg?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/Python/blob/master/images/Image_3.jpg?raw=true" /></a></p>

Notice that Geany is keeping track of the variable that you created on the left side of the screen.

When you execute the command you will see the same results as the first iteration. Variables are helpful when you need to use the same information multiple times in the same program. 

Python has a few rules for variables:
-	Variable names can only include letter, numbers, or underscores, but cannot start with a number.
-	Spaces are not permitted.
-	The names of python methods and functions are reserved, meaning that they cannot be used as variable names. So, print cannot be used as a variable name.
- As a rule, variable names should be short and descriptive.

<blockquote>Q1: In your own words, explain the difference between the print(hello) command we just used and print(“hello”).</blockquote>

# Task 2: Working with Strings and Variables

Python has a few built-in functions for working with strings. Create a new file called name.py in Geany. Assign your first and last name to the variable name in all lower-case letters.

```Python
name = "katie walden"
```

Next, we’ll use the `print` function with the method `title`. Python functions and methods always end with a `()`. Methods define an additional action that can be applied to the data.

```Python
name = "katie walden"
print(name.title())
```

Your program should output your data with a leading capital letter.

We can also change the case using the upper method and lower method: `print(name.upper())` outputs your string with all capital letters, while `print(name.lower())` outputs your string in all lower case.

`Katie Walden`
`KATIE WALDEN`
`katie walden`

Try adding two additional print functions calling the name variable with each of these methods.  

<blockquote>Q2: Describe the syntax three commands that we just used in your own words. Define the function and method for each example.</blockquote>

```Python
first_name = "katie"
last_name = "walden"
full_name = first_name + " " + last name
```

Let’s modify our code a bit and create two new variables `first_name` for your first name and `last_name` for your last name. We can then combine these two string variables (called concatenation) in a third variable called `full_name`.

If we want our first and last name to be separated by a space, we need to tell Python to add one in by including the `“ “`, otherwise, each string will be printed back-to-back.

```Python
first_name = "katie"
last_name = "walden"
full_name = first_name + " " + last name

print(full_name)
```

We can then use the `print` function as we did before to output `full_name` to the screen.

```Python
first_name = "katie"
last_name = "walden"
full_name = first_name + " " + last name

print("Hello, " + full_name.title() + "!")
```
We could combine strings and variables in the same `print` function to output a full sentence to the screen.

```Python
first_name = "katie"
last_name = "walden"
full_name = first_name + " " + last name

sentence="Hello, " + full_name.title() + "!"

print(sentence)
```
We could also assign this whole sentence to a variable and return the same output.

<blockquote>Q3: Explain how each of these two programs (above) work in your own words.</blockquote>

# Task 3: Working With Numbers

Python works with integers (whole numbers) and floats (any number with a decimal point). Python uses the basic mathematic symbols to perform functions: + (add), - (subtract), * (multiply), / (divide). 

Try this program:

```Python
print(2+3)
print(2-3)
print(2*3)
print(2/3)
```

<blockquote>Q4: Why does <code>print(2/3)</code> return 0? How would you modify your code to return the decimal number? Why?</blockquote>

Hint: Try `print(2.0/3.0)` using the floating point integers (numbers with decimal points).

# Task 4: Combining Variable Types

Let’s write a new program with an integer variable and a string variable.

```Python
course_name="The Digital Age"
course_number = 105

print("Welcome to " + course_name.title() + " CSC:" + course_number)
```
When you execute the program, you will receive an error.

<p align="center"><a href="https://github.com/kwaldenphd/Python/blob/master/images/Image_8.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/Python/blob/master/images/Image_8.png?raw=true" /></a></p>

The type error is telling us that we cannot use these two different variable types in the same function. 

When we want numbers to be read as characters rather than numeric digits, we have to use the string method `str()` to convert the integer into a string of characters.

```Python
print("Welcome to " + course_name.title() + " CSC:" + str(course_number())
```

# Task 5: Creating Lists

In our last project we stored information in XML files. Python allows us to store information in a few different ways. 

Let’s start with lists. Lists are an ordered collection of items. Lists can be numbers or strings. They are declared with a variable name, but the information is contained within `[ ]` and the individual items are separated by a comma. 

Write a list of a few of your favorite things.

```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
```

We can print this list with a print function `print(cookies)`, but Python returns a representation of the list, just as we entered it.

`['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']`

This isn’t particularly useful by itself; however, we can use the position of each item (called the *index*) to perform different functions.

Add a print function calling a specific item on your list.

```Python
print(cookies[0].title())
```

This command returns the first item on my list. This is the item in the `0` position on my list.

```Python
Chocolate Chip
```
Items in a list are indexed with a number, **beginning with 0 NOT 1.**

A `print` command that outputs the last item on my list of four items would look like this.

```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
print(cookies[3].title())
```

We can also work backwards on our list using negative numbers. For example, to call the last item on the list we could also use the index position `-1`.

```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
print(cookies[-1].title())
```

To return the second to last item, we could use -2. For the third to last -3, etc. etc.

We can concatenate our list items in strings.

```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
print("My favorite cookie to bake is " + cookies[1].title() + ".")
```
Which outputs `My favorite cookie to bake is snickerdoodle.`

We can also change the items in a list. 

Maybe I have a friend who is allergic to peanut butter. I can change the `peanut butter` entry.

```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
cookies[2] = 'oatmeal'
print(cookies)
```
The print function outputs the modified list.
`['chocolate chip', 'snickerdoodle', 'oatmeal', 'sugar']`

We can also add data to our list using the append function.

```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
cookies.append('oatmeal')
print(cookies)
```

The print function now returns a list of five items `[chocolate chip, snickerdoodle, peanut butter, sugar, oatmeal]`

We can also use `append` to create new lists.

```Python
my_pets = []
my_pets.append('Christy Matthewson')
my_pets.append('Smokey Jo Wood')
print(my_bets)
```

In this block of code, we started with an empty list `[]`. Then the next two lines with `append` added new items to the list.

<blockquote>Q6: Create your own list using the program above as an example. Share your code in your notebook as well as the result. What is the number position for each of the items in your list? How would you return the value of the first item? How would you return the value of the last item?</blockquote>

With `append`, items are added to the end of the list. 

The `insert` function allows us to add items to any position in the list.

```Python
fruit = ['apple', 'pear', 'banana']
fruit.insert(1, 'orange')
print(fruit)
```
This block of code adds orange to the second position on the list (index position 1).

The output is `['apple', 'orange', 'kiwi', 'banana']`

Conversely, the `del` statement allows you to delete items from your list using the index number.

The following code will remove orange from the list.

```Python
fruit = ['apple', 'orange', 'pear', 'banana']
del fruit[1]
print(fruit)
```

We can also delete items by value (instead of position) using `remove`.

```Python
fruit = ['apple', 'orange', 'pear', 'banana']
fruit.remove('orange')
print(fruit)
```

<blockquote><code>remove</code> only removes the first instance of the value in the list. So, if in the previous example orange appeared on the list a second time, only the first instance would be removed. To remove all instances, you would need to perform a loop (we’ll talk about this shortly).</blockquote>

## A few additional functions that can be useful when working with lists.

### `Reverse`

To print in reverse order, use `reverse`.

```Python
fruit = ['apple', 'orange', 'pear', 'banana']
fruit.reverse()
print(fruit)
```

### `Sort`

To alphabetize your list, use the `sort` method.

```Python
fruit = ['apple', 'orange', 'pear', 'banana']
fruit.sort()
print(fruit)
```

### `Len`

To find the length of your list, use the `len` function.

```Python
fruit = ['apple', 'orange', 'pear', 'banana']
length = len(fruit)
print(length)
```

<blockquote>Q7: What is an alternative way to write the `print` command to return the length of the list. *Hint* you’ll combine the last two lines of the example above.</blockquote>

# Task 6: Lists of Numbers

We can also work with numbers in lists. 

We can create a list in the same way that we did in the previous example, or we can use the range function.

```Python

#In this example we'll wrap the list() function around the range() function to create a list of numbers

numbers = list(range(1,10))
print(numbers)
```

This outputs `[1, 2, 3, 4, 5, 6, 7, 8, 9]`

You may have expected to see the numbers one to ten printed. This is yet another example of the quirks of working with programming languages. 

Python starts with the first number and quits when it reaches the last number of your range. Because it stops at 10, it doesn’t include the 10.

<blockquote>Q8: How would you modify this code to output the full range 1-10?</blockquote>

What if we just wanted the odd numbers in this range? We could add an additional value to the `range` function to tell the computer to count by two.

```Python
numbers = list(range(1,11,2))
print(numbers)
```
<blockquote>Q9: How would you rewrite the code to include only the even numbers from 1 to 10?</blockquote>

Can you write a program that creates a list that represents all of the different patterns we could represent from 1 bit to 8 bits, like our chart from binary math lab?

- 1 bit - 2 patterns
- 2 bits - 4
- 3 bits - 8
- 4 bits - 16
- 5 bits - 32
- 6 bits - 64
- 7 bits - 128
- 8 bits - 256
- n bits -2<sup>n</sup> patterns

Try to write a program that outputs the list: `[2, 4, 8, 16, 32, 64, 128, 256]`.

<blockquote>Hint: a double * represents exponents in Python. So 2<sup>2</sup> would be <code>2**2</code>.</blockquote>

There are multiple ways to achieve this output.

```Python
patterns = []
for bit in range(1,9):
  patterns.append(2**bit)
print(patterns)
```

<blockquote>Q10: Either include a snippet of your version of this program in your notebook and explain your code, AND/OR explain how the example version of this program works.</blockquote>

Python also allows us to return the minimum value, maximum value, and sum of the numbers in a list.

```Python
patterns = []
for bit in range(1,9):
  patterns.append(2**bit)

print(min(patterns))
print(max(patterns))
print(sum(patterns))
```

This program outputs
`2`
`256`
`510`

# Task 7: Working With Loops

Loops are one of the most common computer functions (we used a loop last week in our XML transformation). 

In a loop, the computer will continue to follow the instructions, until it can’t perform that function any longer. We’ll use a list to write our first loop.

```Python
#loops through a list of the members of the House Stark.

characters = ['Arya', ' Benjen', 'Bran', 'Catelyn', 'Eddard', 'Rickon', 'Robb', 'Sansa']

for character in characters:
  print(character.title() + "Stark")
```

<blockquote>Note: I used the # to create a comment and describe the purpose of this python program. Comments are written for the human users of the program and will not be processed as code by the computer. Every programming language uses a different set of symbols to designate comments in the code. It’s good practice to include comments in your code so that you code can be modified and reused.</blockquote>

<blockquote>Note the use of the plural for the name of the list and the singular for the individual item is not required. We are just declaring variables here. I could have used anything to name the individual items (e.g. for person in characters). All you are doing with this step is setting a new variable for the individual item. It is standard convention to use the plural and singular terms so that the person reading the code can interpret what it is doing.</blockquote>

The loop command steps through the list one value at a time. The loop continues until it reaches the end of the list. 

In this case, for each item in the list called “characters” the program prints the value of each “character” in the list concatenated with the string “ Stark”. This produces the output:

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

Now let's look at a different loop.

```Python
characters = ['Arya', ' Benjen', 'Bran', 'Catelyn', 'Eddard', 'Rickon', 'Robb', 'Sansa']
print('Members of the House Stark:')
for character in characters:
  print(character.title() + " Stark")
print(characters[0].title() + " is my favorite.")
```

<blockquote>Q11: What do you expect this code to output? Explain how this program works in your own words.</blockquote>

Comments that walk through each line of this program:

```Python
#this line creates the list of character names
characters = ['Arya', ' Benjen', 'Bran', 'Catelyn', 'Eddard', 'Rickon', 'Robb', 'Sansa']

#this first print command prints a header for my list "Members of the House Stark"
print('Members of the House Stark:')

#here is the loop from the previous example
for character in characters:
  #the indentation is important here. This indent indicates that this print command is part of the loop
  print(character.title() + " Stark")
  
#this line is not indented, so it is executed after the loop is complete.  
print(characters[0].title() + " is my favorite.")
```

# Task 8: If...Statements

If-then statements are another common computer function. If statements are conditional, meaning that there is a test to determine if a statement is true or false and then the computer takes some defined action.

```Python
#here is a list of names
names=['department of computer science', 'computer science department', 'cs']

#here is a loop. I am telling Python to look at each of the items in this list
for name in names:

  #this indent tells Python that this next action is part of the loop
  #this is my if statement. Note that like a loop it ends in a colon (:)
  #the double == is an equality operator. It's a boolean test (returns TRUE or FALSE)
  if name == 'cs':

    #if the value is equal to cs, then the conditional statement returns TRUE and the value is printed in all upper case letters
    print(name.upper())

  #the else statement gives the set of instructions for a FALSE value. Notice that it is indented same as the if statement.
  else:

    #All other values that are not 'cs' are printed as Titles
    print(name.title())
```

This program returns the output
`Department of Computer Science`
`Computer Science Department`
`CS`

This program without the comments:

```Python
names=['department of computer science', 'computer science department', 'cs']

for name in names:
  if name == 'cs':
    print(name.upper())
  else:
    print(name.title())
```

<blockquote>Q12: Did the program return the results that you expected? Explain the output in your own words.</blockquote>

Python uses a variety of Boolean Operators – these are the conditional tests that return a True or False.

```Python
#set the variable number to 10
number = 10

#the following statements will return true or false

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

We can also test for values in a list.

```Python
fruits = ['apple', 'pear', 'orange']

#a test to see if apple is on the list
if 'apple' in fruits:
  print('Would you like an apple?')
else:
  print('Sorry, we are all out of apples.')

#a test to see if banana is NOT on the list
if 'banana' not in fruits:
  print('Yes, we have no bananas')
else:
  print('Would you like a banana?')
```

<blockquote>Q13: Explain what this program will output and why.</blockquote>

# Task 9: Gathering Input

So far we’ve written programs that have included the data being processed, but many programs ask for input from their users. 

The `raw_input` function allows you to prompt a user for string-based information. 

```Python
name = raw_input("Please enter your name: ")
print("Hello, " + name)
```
<blockquote>Q14: What did the program output? Explain this program in your own words.</blockquote>

Here we set the variable name to the input that we receive from the user. 

The text in the `()` following the `raw_input` function provides the prompt for the user. We can then reuse the name variable in the `print` function.

Now let’s try an example with numbers. The following program sets a number and asks the user to guess the number.  Notice that we use the `input()` function for integers.

```Python
#sets variable secret_number
secret_number = 3

#asks the user for a number. NOTE we use input instead of raw_input for integers
number = input("Guess a number between 1 and 10: ")

#sets up a loop that will continue to run while the number does not match the secret number
while number !=secret_number:

  #sets up conditional statements that return clues for the user
  if number == secret_number + 1 or number == secret_number -1:
    print("You are really close!")

  #NOTE that the elif statement here stands for "else if"
  #you want to use elif if you have more than two conditions
  elif number < secret_number:
    print("Too low!")

  else:
    print("Too high!")

  #tells the user to input a new number to guess again
  number = input("Guess again: ")

#prints when the user guesses the right number
print("You guessed it!")
```

Program without the comments.

```Python
secret_number = 3

number = input("Guess a number between 1 and 10: ")

while number !=secret_number:
  if number == secret_number + 1 or number == secret_number -1:
    print("You are really close!")
  elif number < secret_number:
    print("Too low!")
  else:
    print("Too high!")
  number = input("Guess again: ")

print("You guessed it!")
```

<blockquote>Q15: Modify the code to change the range to have the user guess between 1 and 100. Then, change the conditional statement to return a “really close” message if they are within a 3 digit range of your number. Include the code in your notes and explain how the program works in your own words.</blockquote>

# Task 10: Describing Data With Dictionaries

We’ll return to inputs, loops, and conditional statements in a minute. Let’s look at another way of storing information with Python. 

In the last lab, we created metadata using XML to describe the information about each of the items we selected for the HTML project. We can also store this metadata in Python using a Dictionary.

```XML
<books>
  <book>
    <title>CSS: The Definitive Guide</title>
    <author>Eric Meyer</author>
    <year>2007</year>
  </book>
  <book>
    <title>Learning XML</title>
    <author>Erik Ray</author>
    <year>2003</year>
  </book>
</books>
```

For now, let’s work with the first example

```XML
<book>
  <title>CSS: The Definitive Guide</title>
  <author>Eric Meyer</author>
   <year>2007</year>
</book>
```
This section of XML has a few different pieces of information about one of the items in a collection. We couuld create a list to hold all of this information.

```Python
book=["CSS: The Definitive Guide", "Eric Meyer", "2007"]
```

But, we lose some meaning here. This now looks like an arbitrary list of information about a work. 

In this example, a list just isn’t powerful enough to store our data. A Dictionary allows us to keep the associated descriptors for each of the items, or the metadata schema that we generated in the last project.

A dictionary uses a slightly different syntax.

```Python
book={'title': 'CSS: The Definitive Guide', 'author': 'Eric Meyer', 'date': '2007'}
```
As with a list, we assign a variable to our dictionary. In this example the variable is `work`. 

The data for the dictionary is wrapped in braces `{ }` rather than the brackets used in a list. 

The information is added in a series of pairs called key-value pairs. Each key is the equivalent of the XML tag and each value equal to the value we associated with the tag.

<blockquote>Q16: Create a dictionary for one of the items in your collection using the tags and information from your XML file. Write a print command and explain the output of your program in your own words.</blockquote>

Just like with the list, we can also create a loop to return each of the values in my new dictionary.

```Python
book={'title': 'CSS: The Definitive Guide', 'author': 'Eric Meyer', 'date': '2007'}

for key, value in book.items():
  print("Key: " + key)
  print("Value: " + value)
```
This program returns the output:

```Python
Key: date
Value: 2007
Key: author
Value: Eric Meyer
Key: title
Value: CSS: The Definitive Guide
```

This program assigns the variable `key` to the key and `value` to the value for each key-value pair. We could use any variables for key and value.

The following program will return the same output:

```Python
for tag, data in book.items():
  print("Key: " +tag)
  print("value: " + data)
```

<blockquote>Q17: Try the following two programs. What did the programs output? Explain how each program works in your own words.</blockquote>
  
```Python
for tag in book.keys():
  print(tag)
```
and 

```Python
for data in book.values(): 
    print(data)
```  
  
Like with lists, we can start with an empty dictionary and add values.
  
```Python
book={}
book['title']='CSS: The Definitive Guide'
book['author']='Eric Meyer'
book['date']='2007'
  
print(book)
```
  
This program outputs `{'date': 2007, 'author': 'Eric Meyer', 'title': 'CSS: The Definitive Guide'}`
  
We can modify elements in the dictionary and add new elements in the same way.
  
```Python
book={'title': 'CSS: The Definitive Guide', 'author': 'Eric Meyer', 'date': '2007'}
  
#modify the date to 2002
book['date'] = 2002
  
print(book)
```
  
<blockquote>Q18: What do you expect this program to output? Why?</blockquote>
  
We can also delete key-value pairs using the `del` function.
  
```Python
book={'title': 'CSS: The Definitive Guide', 'author': 'Eric Meyer', 'date': '2007'}
  
del book['title']
 
print(book)
```

This outputs `{'date': '2007', 'title': 'CSS: The Definitive Guide'}`

We can also check to see if a key or value is in the dictionary.

```Python
book={'title': 'CSS: The Definitive Guide', 'author': 'Eric Meyer', 'date': '2007'}

if 'title' not in book.keys():
  print("The Title is missing.")

if 'HTML' not in book.values():
  print("The title is " + work['title'])
```

<blockquote>Q19: Explain the if functions in your own words. What does this program output? Why?</blockquote>

# Task 11: Nesting Dictionaries

As we just demonstrated, dictionaries have different afforedances than lists. 

But, we’ve described three different objects in our collection using lists. What could be involved in transforming these lists into dictionaries?

```XML
<books>
  <book>
    <title>CSS: The Definitive Guide</title>
    <author>Eric Meyer</author>
    <year>2007</year>
  </book>
  <book>
    <title>Learning XML</title>
    <author>Erik Ray</author>
    <year>2003</year>
  </book>
</books>
```

One way to accomplish this goal with Python would be to generate two different dictionaries.

```Python
book_0={'title': 'CSS: The Definitive Guide', 'author': 'Eric Meyer', 'date': '2007'}
book_1={'title': 'Learning XML', 'author': 'Erik Ray', 'date': '2003'}
```

We could then use a list to generate a list of the metadata for each of the works.

```Python
book_0={'title': 'CSS: The Definitive Guide', 'author': 'Eric Meyer', 'date': '2007'}
book_1={'title': 'Learning XML', 'author': 'Erik Ray', 'date': '2003'}

books = [book_0, book_1]
print(books)
```

While the this program outputs all of the metadata, one of the advantages of our XML file is that all of the information was stored in a single place.

Another solution would be to embed a list in a dictionary.

```Python
books = {
  'title': ['CSS: The Definitive Guide', 'Learning XML']
  'date': ['2007', '2003']
  'author': ['Eric Meyer', 'Erik Ray']
  }

print ("My books include books by " + books['author'] + ":")
for title in books['title']:
  print("\t" + title)
```

This program outputs:

```
My books include books by Eric Meyer and Erik Ray:
  CSS: The Definitive Guide
  Learning XML
```

<blockquote>Note: The <code>\t</code> is a short cut for a TAB so that my list was indented. <code>\n</code> will generate a new line in your output.</blockquote>

While this dictionary contains all of the data from my XML, there are some limitations. The dates are not specifically connected to the title that they are associated with. We can solve this problem by nesting a dictionary in a dictionary.

```Python
books = {
  'CSS: The Definitive Guide': {
    'date': '2007', 
    'author': 'Eric Meyer'
    },
  'Learning XML': {
    'date': '2003',
    'author': 'Erik Ray'
    }
}
```

This example includes a dictionary called `books` that holds two other dictionaries. It uses the title as the key for each of the dictionaries for the works. The value of each of these keys is a dictionary containing “title”, “date”, and "author.”

The following program will output the titles of items in this collection as well as associated dates.

```Python
print("My Books: ")
for book, book_info in books.items():
  full_title = book + " (" + book_info['date'] + ")"
  print("\t" + full_title_title())
```
This program prints the title first as a separate line. The `for` loop digs into the data for each of the books. 

`book` is the variable assigned to each of the keys in the `books` dictionary - in this example it is the titles of each of the books. 

`book_info` is the variable assigned to each of the values. `method .items()` works through each of the dictionaries. 

The next line, assigns a variable `full_title` that concatenates each work variable with an opening `(`, the date for each work called with `book_info[‘date’]`, and a closing `)`. 

The final line prints a tab `\t` before each concatenated string that we just created with the `full_title` variable.

This outputs:

```
My Books:
  CSS: The Definitive Guide (2007)
  Learning XML (2003)
```

<blockquote>Q20: Write a similar dictionary for your XML file and generate some output. Copy and paste your code and your result into your notebook. Explain how your program works in your own words.</blockquote>

# Task 12: Parsing XML With Python

You may be thinking, “…but we already have an XML file with this data in it. Can we use Python to with .xml?” The answer to this question is YES! 

In this next task, we’ll use the ElementTree API https://docs.python.org/3/library/xml.etree.elementtree.html. This is part of the Python library that has been written specifically to parse XML. 

We’ll only work with a few functions and methods from ElementTree as an introduction to the tool.

```XML
<?xml version="1.0" encoding="UTF-8"?>
<books>
  <book>
    <title>CSS: The Definitive Guide</title>
    <author>Eric Meyer</author>
    <year>2007</year>
  </book>
  <book>
    <title>Learning XML</title>
    <author>Erik Ray</author>
    <year>2003</year>
  </book>
</books>
```

First, we need to import the ElementTree module into our file so that we can continue to use the methods and functions associated with ElementTree. Type this first line of code into a new file called `XML.py` (or whatever you’d like to call it).

```Python
import xml.etree.cElementTree as ET
```

Now we need to import our .xml file. Remember, you’ll need to include the entire file path for your .xml file if it is not in the same folder as your python file.

```Python
import xml.etree.cElementTree as ET
tree = ET.parse('books.xml')
```
And, finally, we need to get the root element of our xml file. Remember in our last project we also had to name the root element in our XSL file. This tag that is at the top of the hierarchy. In the example file, the root is `<books>`.

```Python
import xml.etree.cElementTree as ET
tree = ET.parse('books.xml')
root = tree.getroot()
```

Now we are ready to work with our .xml file in Python. Try adding `print` commands.

```Python
import xml.etree.cElementTree as ET
tree = ET.parse('books.xml')
root = tree.getroot()

print(root.tag)
print(root.attrib)
```

This program returns the output:
```
books
{}
```

This set of commands returns the tag for the root element `books` and an empty set of braces for the attribute because there is not an attribute associated with the `books` tag. 

You probably didn’t assign attributes to your XML tags, so we’ll keep working with tags. If you have attributes in your file, you can consult the documentation for ElementTree to modify your code.

This code gave us the root element, but what if we want to see the structure of our document? We can use the `iterator` function to pull all of the elements from our XML file in a simple loop that outputs each tag and the text value associated with it.

```Python
import xml.etree.cElementTree as ET
tree = ET.parse('books.xml')
root = tree.getroot()

iter = root.getiterator()

for element in iter:
  print element.tag, element.text
```

This program outputs:
```
books

book

title CSS: The Definitive Guide
date 2007
author Eric Meyer
book

title Learning XML
date 2003
author Erik Ray
```

Now let’s get some data from the file. This next program creates a loop that returns all the titles in the file. 

In the sample XML file, `<book>` tag is the child of `<books>` and `<title>` is a child of `<book>`. 

This loop says for each work, assign text from the `title` element to the variable `title`, and then print the titles.

```Python
import xml.etree.cElementTree as ET
tree = ET.parse('books.xml')
root = tree.getroot()

for book in root.findall('book'):
  title = book.find('title').text
  print(title)
```

This program outputs:
```
CSS: The Definitive Guide
Learning XML
```
But what if we want to pull the title and date? We can modify the code to also pull the information from the `<date>` tag.

```Python
import xml.etree.cElementTree as ET
tree = ET.parse('books.xml')
root = tree.getroot()

for book in root.findall('book'):
  title = book.find('title').text
  date = book.find('date').text
  
  print(title)
```

<blockquote>Q21: What do you expect this program out output? Why? Explain how this code works in your own words.</blockquote>

<blockquote>Q22: Write a similar program for the .xml file that you created in the last exercise. Pull data from at least two elements. Copy your code and your output in your notebook and explain what your code does (or is attempting to do).</blockquote>

# Lab Questions

All of the required questions are listed here. Be sure to answer each question completely, including an explanation of how you arrived at your answer.

Q1: In your own words, explain the difference between the `print(hello)` command we just used and `print(“hello”)`.

Q2: Describe the syntax three commands that we just used in your own words. Define the function and method for each example.

Q3: Explain how each of these two programs (above) work in your own words.

Q4: Why does `print(2/3)` return 0? How would you modify your code to return the decimal number?

Q5: Explain `concatenation` in your own words. Why must we convert numbers to strings in the program above? Refer to this example and the previous example.

Q6: Create your own list using the program above as an example. Share your code in your notebook as well as the result. What is the number position for each of the items in your list? How would you return the value of the first item? How would you return the value of the last item?

Q7: What is an alternative way to write the `print` command to return the length of the list. *Hint* you’ll combine the last two lines of the example above.

Q8: How would you modify this code to output the full range 1-10?

Q9: How would you rewrite the code to include only the even numbers from 1 to 10?

Q10: Either include a snippet of your version of this program in your notebook and explain your code, AND/OR explain how the example version of this program works.

Q11: What do you expect this code to output? Explain how this program works in your own words.

Q12: Did the program return the results that you expected? Explain the output in your own words.

Q13: Explain what this program will output and why.

Q14: What did the program output? Explain this program in your own words.

Q15: Modify the code to change the range to have the user guess between 1 and 100. Then, change the conditional statement to return a “really close” message if they are within a 3 digit range of your number. Include the code in your notes and explain how the program works in your own words.

Q16: Create a dictionary for one of the items in your collection using the tags and information from your XML file. Write a `print` command and explain the output of your program in your own words.	

Q17: Try the following two programs. What did the programs output? Explain how each program works in your own words.
  
```Python
for tag in book.keys():
  print(tag)
```
and 

```Python
for data in book.values(): 
    print(data)
```  
  
Q19: Explain the `if` functions in your own words. What does this program output? Why?

Q20: Write a similar dictionary for your XML file and generate some output. Copy and paste your code and your result into your notebook. Explain how your program works in your own words.

Q21: What do you expect this program out output? Why? Explain how this code works in your own words.

Q22: Write a similar program for the .xml file that you created in the last exercise. Pull data from at least two elements. Copy your code and your output in your notebook and explain what your code does (or is attempting to do).
