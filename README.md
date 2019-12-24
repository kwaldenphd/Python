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

[IMAGE]

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

Notice that as with our other HTML and XML projects, Geany has highlighted the syntax for us to make debugging easier.

[IMAGE]

Now we need to run the file – either press F5 or select Build > Execute from the menu. A terminal window should open with the phrase “Hello World!”

You have just successfully written your first Python program. What just happened? 

When you select Execute from the menu, Geany runs the file through the Python interpreter, this is another program that reads though the Python code that you just wrote and determines what each piece of code means and then executes the code (or runs it). 

In this example, the Python interpreter recognizes the word print as a Python function. This function allows you to “print” to the screen or send output to the computer screen. 

The brackets () contain the information to be printed. In this case you have entered a string “Hello World.” 

<blockquote>A string is any series of characters. Strings are identified by the “ ” or alternatively by ‘ ’.</blockquote>

Let’s change this program a bit. We are going to assign our first variable. A variable is a placeholder for a piece of information. You can think of it as a basket or container. 

Let’s modify the code as follows:

```Python
hello="Hello World"
print(hello)
```

[IMAGE]

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

Next, we’ll use the print function with the method title. Python functions and methods always end with a (). Methods define an additional action that can be applied to the data.

```Python
name = "katie walden"
print(name.title())
```

[IMAGE]

Your program should output your data with a leading capital letter.

We can also change the case using the upper method and lower method: `print(name.upper())` outputs your string with all capital letters, while `print(name.lower())` outputs your string in all lower case.

`Katie Walden
KATIE WALDEN
katie walden`

Try adding two additional print functions calling the name variable with each of these methods.  

<blockquote>Q2: Describe the syntax three commands that we just used in your own words. Define the function and method for each example.</blockquote>

```Python
first_name = "katie"
last_name = "walden"
full_name = first_name + " " + last name
```

Let’s modify our code a bit and create two new variables `first_name` for your first name and `last_name` for your last name. We can then combine these two string variables (called concatenation) in a third variable called `full_name`.

If we want our first and last name to be separated by a space, we need to tell Python to add one in by including the “ “, otherwise, each string will be printed back-to-back.

```Python
first_name = "katie"
last_name = "walden"
full_name = first_name + " " + last name

print(full_name)
```

We can then use the print function as we did before to output `full_name` to the screen.

```Python
first_name = "katie"
last_name = "walden"
full_name = first_name + " " + last name

print("Hello, " + full_name.title() + "!")
```
We could combine strings and variables in the same print function to output a full sentence to the screen.

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
