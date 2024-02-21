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

### Common problems with variables

Python won't understand your program if you try to put spaces in your variable names. You can use these tricks so your variable names don't have spaces:

```python
use_underscores_instead_of_spaces
pushallthewordstogether # but this is hard to read
useCapitalLetters
```

Python can get confused if you use a variable name that is already used for something else e.g. `print`, `for`, `import`.

When you use a variable name you must match it exactly. Python won't understand if you use capital letters in one place and not the other. For example:

```python
myVariable = 10
print(myvariable) # Python won't work out that you meant to have a capital V
```

### Practice with variables

Use a python editor to try these exercises:

- Make a variable called "height" and give it a value (e.g how tall are you?)
- Print the variable
- Try printing a variable we havent made like "great_height". What happens?
- Now make a variable called "great_height" and make it 10 times the size of "height"
- Print "great_height"

### Learning more about variables:

- There is lots more to learn about variables. You can search for more help online or just look at [w3schools](https://www.w3schools.com/python/python_variables.asp).
- Once you feel ok with variables you can learn more about [data and types of data in Python](https://www.w3schools.com/python/python_datatypes.asp)

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

- `def` is a special key word which is short for "define" and tells python that we want it to remember a function
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

### Common problems with functions:

- Just like variable names, Python won't understand function names with spaces.
- It is easy to forget the `:` at the end of the `def` line or forget the brackets.
- Check how you have indented (shifted right) the lines, especially if your function contains some of the [control statements](#writing-less-code-and-reacting-to-events) we cover later.
- Check how you are using the special input variables. The `def` line will show you how many inputs the function needs and in what order. When you use the function later in your programme you need to give it the right inputs in the right order.
- If your function needs to give back a result think about if the result needs to be given back to Python code with `return the_result` or to a human with `print(the_result)` or maybe both.

### Practice with functions

Use a Python editor to try these exercises:

- Make a function called "add1" which takes one number as an input, adds 1 to it and gives back the result
- Test your function by giving it some numbers and printing the results
- Do the same again but with an "adder" function which takes two inputs and adds them together

There are other sorts of subprogram in Python but make sure you are really confident with functions first. When you are ready look at [modules](https://www.w3schools.com/python/python_modules.asp), [classes](https://www.w3schools.com/python/python_classes.asp) and [lambdas](https://www.w3schools.com/python/python_lambda.asp)

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

- Subprograms or functions that we have [seen already](#small-helper-programs). You can write some code, wrap it up in a function and re-use the same code many times. Your function can have a helpful name which makes the code easier to understand and you can use inputs so that the function can do different things in different circumstances.
- [Branches](https://www.enjoyalgorithms.com/blog/conditions-and-branching-in-python). We will cover these later. Branches allow your program to go down different paths depending upon an input. That could be from a person using the program, from some kind of sensor or from somewhere else in the program.
- Loops and repetition. We will cover these later too. These let you write one bit of code and use it many times.

It is normal to use all of these structures in your program. All programing languages have these structures but they might use different key words, punctuation and layouts for them.

### Switching between different bits of code

You programme can do different things in different circumstances. Here is a simple example.

```python
your_age = int(input("Enter someone's age:"))
print('You have entered: ', your_age)
if your_age < 16:
    print('A responsible adult needs to stay with them at a TechJam')
print('Thank you')
```

The `print` command is in a branch of code. Python checks the value saved in the variable `your_age` and only used the branch if the value is less than 16. Otherwise, the Python skips past the branch and carries on. You tell Python which lines are part of the branch by indenting them (shifting right).

Here is a slightly different example with two branches.

```python
your_age = int(input("Enter someone's age:"))
print('You have entered: ', your_age)
if your_age < 16:
    print('A responsible adult needs to stay with them at a TechJam')
else:
    print('They can stay at TechJam on their own, but only if they act responsibly!')
print('Thank you')
```

You can have lots of branches. Here is an example with three.

```python
your_age = int(input("Enter someone's age:"))
print('You have entered: ', your_age)
if your_age == 0:
    print('Are you sure? They might be a little too young for TechJam')
elif your_age < 16:
    print('A responsible adult needs to stay with them at a TechJam')
else:
    print('They can stay at TechJam on their own, but only if they act responsibly!')
print('Thank you')
```

You can have any number of lines of code in each branch. Just like for functions you use indents (shift the line to the right) so that Python can see where the branch starts and finishes.

### Common problems with branches:

- Check how you have indented (shifted right) your lines of code, especially if you are using branches with other things such as [functions](#small-helper-programs) or [loops](#tbc).
- it is easy to forget the `:` at the end of the `if`, `elif` and `else` lines.
- It is easy to put `=` (which means define or update a [variable](#remembering-and-naming-things)) when you really meant to put `==` (which means tell me if these two things are the same).
- You only need to add a few branches to make your program complicated and hard to understand. It can be an good idea to try out small parts of your program on their own and check they do what you expect before you put them all together. It can be easier to understand if you split complicated code into several small helper functions.
- It is easy to make mistakes if you have big branches with lots of code in them. If you are getting stuck try breaking up a big branch into sections and move the sections into a helper function with a helpful name.

### Practice with branches

Try out the example branches in your Python editor and change them to see what happens. Here are some extra things to try:

- At the end of each example is a `print('Thank you')` line:

  - What do you think will happen if you indent (shift right) this line by mistake?
  - Try it and see if you are right.
  - Can you explain what is going on?

- Try out the example with three branches:

  - Try swapping the `== 0` and `< 16` around.
  - What happens when you enter `0` for the age now?
  - Can you work out why?
  - Can you think of some more branches and add them?

- Make a quiz program which poses some questions and uses branches to check the answers and either give congratulations or the correct answer.
- Extend your quiz program by adding a variable to keep score and increase the score each time someone gives a correct answer.

#### Learn more about branches

There is lots more to learn about branches. You can search online or look at [W3Schools](https://www.w3schools.com/python/python_conditions.asp)

There are some more advanced kinds of branches to investigate. Make sure you can use if-statements first. When you are ready have a look for `match ... case` statements and `try ... except` statements.


