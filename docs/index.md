# After your first steps with Python

At the [TechJams](https://techjam.softwarecornwall.org/) you can get started with the [Python](https://www.python.org/) programing language by working through some of our pre-prepared exercises. In these exercises you will have used things like [variables](https://www.w3schools.com/python/python_variables.asp), [functions](https://www.w3schools.com/python/python_functions.asp) and [control flow](https://www.w3schools.com/python/python_for_loops.asp) but you might not have realised what these can do. As you take on your own projects it will really help if you understand these things a little more so that you can use them yourself.

This guide assumes you are coding with Python but other programing languages do things in similar ways.

## Using a Python workspace

### Raspberry Pi

[Thonny](https://thonny.org/) is usually already installed and can be used for these exercises

### PC

You can install [Thonny](https://thonny.org/) on a PC or search for 'Python' in your PC's App Store

### Web

There are quite a few online Python editors available. You can search for one yourself or just try [Programiz](https://www.programiz.com/python-programming/online-compiler/)

## Remembering and naming things

Variables are a way for your programs to remember or save information and give them a name so that they are easier to use. Here is an example:

```python
number_of_columns = 10
```

This makes a variable called "number_of_columns" and saves the number 10 in it. If you need the number of columns somewhere in your programme you can use this variable. For example:

```python
for next_column in range(number_of_columns):
  ...
```

or

```python
number_of_cells = number_of_columns * number_of_rows
```

The simplest way to make a variable is with an assignment statement that follows this pattern

```python
variable_name = value_to_remember
```

Later we will see that other statements can create special variables. For example, the code we saw earlier:

```python
for next_column in range(number_of_columns):
```

This makes a special variable called "next_column" which we can use inside the "for" loop.

### Practice with variables

Use a python editor to try these exercises:

- Make a variable called "height" and give it a value (e.g how tall are you?)
- Print the variable
- Try printing a variable we havent made like "great_height". What happens?
- Now make a variable called "great_height" and make it 10 times the size of "height"
- Print "great_height"

### Learning more about variables

There is lots more to learn about variables. You can search for more help online or just look at [w3schools](https://www.w3schools.com/python/python_variables.asp).

## Small helper programs

Functions are small programs which help you make bigger, more complicated programmes. You will have already used some functions that are built into Python or added in with an `import`. You can also make these yourself. Here is a simple example:

```python
def double_it(original_value):
  new_value = original_value * 2
  return new_value
```

This makes a function called "double_it" which takes one input, doubles it and returns the result. Once we have told Python about our helper programme we can use it in lots of different ways. Here are some examples:

```python
print(double_it(5)) # Will print the number 10
child=1.4
giant=double_it(child) # Uses a variable as the input and puts the result in a variable
```

All function definitions follow a similar pattern.

```python
def function_name (names_of_parameter):
  line of code
  line of code #lines of code inside the function
  line of code
  return some_value

line of code # this code is not part of the function
```

Some things to notice:

- `def` is a special key word which is short for "define" and tells python we are going to tell it about a function
- There are always brackets after the function name, even if there is nothing inside the brackets. Brackets help Python understand your are talking about a function rather than the name of a variable.
- The function can take inputs. If we have inputs we have to give each of them a name so we can use them in our helper programme. If you have no inputs we still keep the brackets. If we have more than one we put "," between the input names
- The first line ends with ":" so we know what follows will be a block of code
- Each line in the block of code is moved right (called an indent) with the tab key so Python can tell where the block starts an stops
- We can give back a result by using the special "return" key word with the value we want to give back.
- The lines after your function are not indented so that Python knows where you helper program finishes.

Here are some more helper functions which shows we can make helper functions using other functions.

```python
def multiplyer(first_value, second_value):
  return first_value * second_value

def triple_it(input_value):
  return multiplyer(input_value, 3)
```

### Practice with functions

Use a Python editor to try these exercises:

- Make a function called "add1" which takes one number as an input, adds 1 to it and gives back the result
- Test your function by giving it some numbers and printing the results
- Do the same again but with an "adder" function which takes two inputs and adds them together

### Learning more about functions

There is lots more to learn about functions. You can search for more help online or just look at [w3schools](https://www.w3schools.com/python/python_functions.asp).

## Writing less code and reacting to events

When you write a program Python will normally perform each line in sequence.

```python
line of code # 1st step
line of code # 2nd step
line of code # 3rd step
... # more steps
```

For almost any interesting program this won't be enough on its own. Here are some reasons:

- Sometime you will be working with lots of data and information. If you can only do one step after the other you will have to write lots of boring repetitive code.
- A program is unable to change what it does in response to events - imagine a compute game that ignored the controller!
- Complex programs will be very hard to read - imagine if books didn't have chapters and paragraphs!

Python gives you ways to change the flow of the program so that you can make your code easier to read, quicker to write and react to events. These are sometimes called control structures. The main structures are:

- Subprograms or functions that we have seen already. You can write some code, wrap it up in a function and re-use the same code many times. Your function can have a helpful name which makes the code easier to understand and you can use inputs so that the function can do different things in different circumstances.
- Branches, if-statements and switch-statements. We will cover these later. if-statements allow your program to go down different paths depending upon an input. That could be from a person using the program, from some kind of sensor or from somewhere else in the program.
- Loops and repetition. We will cover these later too. These let you write one bit of code and use it many times.

It is normal to use all of these structures in your program. All programing languages have these structures but they might use different key words, punctuation and layouts for them.
