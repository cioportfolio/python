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

### Practice

Use a python editor to try these exercises:

- Make a variable called "height" and give it a value (e.g how tall are you?)
- Print the variable
- Try printing a variable we havent made like "great_height". What happens?
- Now make a variable called "great_height" and make it 10 times the size of "height"
- Print "great_height"

## Small helper programs

Functions are small programs which help you make bigger, more complicated programmes. Here is a simple example:

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
  #...
  #... lines of code inside the function
  #...
  #... return some_value

#... lines of code not inside the function
```

Some things to notice:
- `def` is a special key word which is short for "define" and tells python we are going to tell it about a function
- There are always brackets after the function name
- The function can take inputs. If we have inputs we have to give each of them a name so we can use them in our helper programme. If you have no inputs we still keep the brackets. If we have more than one we put "," between the input names
- The first line ends with ":" so we know what follows will be a block of code
- Each line in the block of code is moved right (called an indent) with the tab key so Python can tell where the block starts an stops
- We can give back a result by using the special "return" key word with the value we want to give back.

Here are some more helper functions which shows we can make helper functions using other functions.

```python
def multiplyer(first_value, second_value):
  return first_value * second_value

def triple_it(input_value):
  return multiplyer(input_value, 3)
```

### Practice

Use a Python editor to try these exercises:

- Make an function called "add1" which takes one number as an input, adds 1 to it and gives back the result
- Test your function by giving it some numbers and printing the results
- Do the same again but with an "adder" function which takes two inputs and adds them together


