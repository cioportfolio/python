# After your first steps with Python

At the [TechJams](https://techjam.softwarecornwall.org/) you can get started with the [Python](https://www.python.org/) programing language by working through some of our pre-prepared exercises. In these exercises you will have used things like [variables](https://www.w3schools.com/python/python_variables.asp), [functions](https://www.w3schools.com/python/python_functions.asp) and [control flow](https://www.w3schools.com/python/python_for_loops.asp) but you might not have realised what these can do. As you take on your own projects it will really help if you understand these things a little more so that you can use them yourself.

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

### Exercise

Use a python editor to try these exercises:

- Make a variable called "height" and give it a value (e.g how tall are you?)
- Print the variable
- Try printing a variable we havent made like "great_height". What happens?
- Now make a variable called "great_height" and make it 10 times the size of "height"
- Print "great_height"

## Small helper programs

Functions are small programs which help you make bigger, more complicated programmes. Here is a simple example:

```python
def make_giant(original_height):
  new_height = original_height * 10
  return new-height
```

This makes a function called "make_giant" which takes one input and shows the input on the screen with a label.


