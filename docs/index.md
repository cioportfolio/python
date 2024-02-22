# After your first steps with Python

At the [TechJams](https://techjam.softwarecornwall.org/) you can get started with the [Python](https://www.python.org/) programing language by working through some of our pre-prepared exercises. In these exercises you will have used things like [variables](https://www.w3schools.com/python/python_variables.asp), [functions](https://www.w3schools.com/python/python_functions.asp) and [control flow](https://www.w3schools.com/python/python_for_loops.asp) but you might not have realised what these can do. As you take on your own projects it will really help if you understand these things a little more so that you can use them yourself.

This guide includes:

- [Using variables to remember and name things](#remembering-and-naming-things)
- [Using functions to make code shorter and easier to read](#small-helper-programs)
- [Using branches to respond to different events](#switching-between-different-bits-of-code)
- [Using loops to repeat code many times](#repeating-code-many-times)
- [Putting everything together](#mixing-controls-for-big-and-complex-programs)

The sections have some simple explanations and examples, reminders of some common problems, exercises to try and where you can learn more when you are ready.

## Using a Python workspace

Practising is better than just reading so use this section to find a place to practice your Python.

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

### Learning more about variables

There is lots more to learn about variables. You can search for more help online or just look at [w3schools](https://www.w3schools.com/python/python_variables.asp).

Once you feel ok with variables you can learn more about [data and types of data in Python](https://www.w3schools.com/python/python_datatypes.asp).

Python has modules you can `import` for more complex data structures but these are probably for quite advanced programers.

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
- There are always brackets after the function name, even if there is nothing inside the brackets. Brackets help Python understand you are talking about a function rather than the name of a variable.
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

### Learning more about functions

There is lots more to learn about functions. You can search for more help online or just look at [w3schools](https://www.w3schools.com/python/python_functions.asp).

There are other sorts of subprogram in Python but make sure you are really confident with basic functions first. When you are ready look at [modules](https://www.w3schools.com/python/python_modules.asp), [classes](https://www.w3schools.com/python/python_classes.asp) and [lambdas](https://www.w3schools.com/python/python_lambda.asp)

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

## Switching between different bits of code

Your program can do different things in different circumstances. Here is a simple example.

```python
your_age = int(input("Enter someone's age:"))
print('You have entered: ', your_age)
if your_age < 16:
    print('A responsible adult needs to stay with them at a TechJam')
print('Thank you')
```

The second `print` command is in a branch of code. The `if` statement tells Python to check the value saved in the variable `your_age` and only uses the branch if the value is less than 16. Otherwise, Python skips past the branch and carries on. You tell Python which lines are part of the branch by indenting them (shifting right).

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
Things to note:

- The conditions in the `if` and `elif` lines are tried one at a time.
- The first one that is `True` gets used and all the rest are ignored.
- if you have an `else` you can only have a single one and it must be for the last branch. This is used if all of the `if` and `elif` tests are `False`.
- you can have lots of `elif` branches.

You can have any number of lines of code in each branch. Just like for functions you use indents (shift the line to the right) so that Python can see where the branch starts and finishes.

### Common problems with branches:

- Check how you have indented (shifted right) your lines of code, especially if you are using branches with other things such as [functions](#small-helper-programs) or [loops](#repeating-code-many-times).
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

### Learn more about branches

There is lots more to learn about branches. You can search online or look at [W3Schools](https://www.w3schools.com/python/python_conditions.asp)

There are some more advanced kinds of branches to investigate. Make sure you can use if-statements first. When you are ready have a look for `match ... case` statements and `try ... except` statements.

## Repeating code many times

If you are working with lots of information it is easy to have boring repetitive code like this.

```python
LEDStrip[0]=(0,0,0)
LEDStrip[1]=(0,0,0)
LEDStrip[2]=(0,0,0)
... # lots more similar lines
LEDStrip[199]=(0,0,0)
```

If you look carefully, each line is the same except for the index (the number inside the `[]` brackets). We have already learnt about [helper functions](#small-helper-programs) but, in this case it doesn't save us much effort. Here is an example.

```python
def clear(LED_num):
    LEDStrip[LED_num]=(0,0,0)

clear(0)
clear(1)
clear(2)
... # lots of similar lines
clear(199)
```

For this kind of repetition we can use a Python loop instead. Here is the same program using a `for` loop.

```python
for LED_num in range(200):
    LEDStrip[LED_num]=(0,0,0)
```

Things to note:

- `for` is a special key word which tells Python what sort of loop we want. We'll see another type in a moment.
- after the `in` key word we have a list or something which makes a list. In this example we have used the [`range`](https://www.w3schools.com/python/ref_func_range.asp) function to make a list which starts at 0 and goes all the way up to 199 (`range` gives us 200 values but as the first one is 0 the last will be 199).
- `LED_num` is a special variable (we could have called it `next_led`, `counter` or any helpful variable name).
- After the `:` we have a block of indented (shifted right) code just like we might have in a branch or helper function.
- Python will take each item in the list one after the other, update the value in our special variable and run the block of code.

We don't have to use `range` in our loops and we aren't limited to lists of numbers but `for` with a `range` is a very common pattern you will notice quite a lot.

Here is another type of loop we can use in Python which is introduced with the key word `while`. This example looks different to the `for` loop but does exactly the same job.

```python
LED_num = 0
while LED_num < 200:
    LEDStrip[LED_num]=(0,0,0)
    LED_num = LED_num+1
```

Some things to note:

- The `while` key word is followed by a condition which is similar to the condition we might use with branches and `if`.
- The `while` line ends with a `:`
- There is a block of code with indented (shifted right) lines which shows Python what code is repeated by the loop
- Python checks the condition on the `while` line. If the condition is `True` it runs the block of code and checks again
- If the condition is `False` it skips the block of code and carries on after the loop.
- We still have a `LED_num` variable but the `while` loop does not look after it the way that a `for` loop does. We've set it to the correct start value before the loop and change it each time.

In this example the `for` version is a bit easier than the `while` version. In some cases you may find the `while` option better. For example, if you need to step through two lists in parallel a `while` loop will be easier to understand than a `for` loop. Another example is looping forever like this.

```python
While True: # With a capital 'T'. Not 'true'
    ... 
    ... # Repeat this block of code forever!
    ...

... # Python won't get to this code unless we do something special to 'break' out of this loop.
```

### Common problems with loops

Common problems with loops are very similar to the ones you have already seen for [branches](#common-problems-with-branches):

- Check how you have indented (shifted right) your lines of code, especially if you are using loops with other things such as [functions](#small-helper-programs) or [branches](#switching-between-different-bits-of-code).
- it is easy to forget the `:` at the end of the `for` or `while` lines.
- In a `while` loop it is easy to put `=` (which means define or update a [variable](#remembering-and-naming-things)) when you really meant to put `==` (which means check if these two things are the same).
- If Python stops with an error in the loop it can sometimes be hard to spot what is wrong. It might work on some repetitions and not others, for example, if the special loop variable gets too large. [Some Python editors have debug tools](https://cs111.wellesley.edu/labs/lab02/debugger) to help you find these kinds or problem.
- It is easy to make mistakes if you have loops with lots of code in them. If you are getting stuck try breaking up a big block in a loop into sections and move the sections into a helper function with a helpful name.

### Practice with loops

Try out the example loops in your Python editor:

- Use a `for` loop to print all the numbers from 0 to 50
- Can you change your loop to print only the event numbers?
- Can you change your loop to print odd numbers between 10 and 40?
- Create a list of your favourite characters and make a loop to print each character in the list. You can make a list like this

    ```python
    characters = ['Batman', 'Luke Skywalker' .... ]
    ```

- Can you change your loop so that each favourite is preceeded by a line number e.g.

    ```text
    1.Batman
    2.Luke Skywalker
    ...
    ```

- Can you change your loop so that it says 'is better than' between each favourite but not before the first and not after the last favourite in the list? *Hint: You may need to put a branch inside your loop*

### Learn more about loops

There is lots more to learn about loops. You can search online or look at [W3Schools](https://www.w3schools.com/python/python_while_loops.asp). Look for some special key words that work with loops like `break`, `continue`, `else`.

There are some more advanced kinds of loops to investigate. Make sure you can use basic `for` and `while` first. When you are ready have a look for list comprehension and recursion. For advanced Python users there are also iterators and generators.

## Mixing controls for big and complex programs

[Functions](#small-helper-programs), [branches](#switching-between-different-bits-of-code) and [loops](#repeating-code-many-times) are useful on their own but are even more powerful when used together. Earlier we saw how we could use a loop to control lots of LEDs at once. Putting the loop inside a function can make it even easier to use.

```python
def clear_LEDs(): # define the helper function
    for LED in range(200):
        LEDStrip[LED_num]=(0,0,0)

clear_LEDs() # Use the helper function.
```

Things to note:

- The `for` line is indented (shifted right) because it is part of the function. Sometime you will see this refered to as 'nesting'. The `for` loop is nested inside the function.
- The 'LEDStrip' line is indented twice. This is because it is inside a `for` loop and the `for` is already indented once.

Here is an example of using a function and a branch inside a loop.

```python
import keyboard

while True: # Loop forever unless we do something special
    clear_LEDs() # Function used inside a loop
    ...
    ... # more code that might display a pattern
    ...
    if keyboard.read_key() == 'q': 
        # branch to break out of the loop
        break
print("Finished")
```

Things to note:

- Look carefully at how the lines are indented (shifted to the right). The branch is 'nested' inside the loop so all of its lines have an extra indent (extra right shift).
- The 'clear_LEDs' function has a loop inside it. We could put the loop here directly but using the function is easier to understand and doesn't have extra indents.

You can combine or 'nest' functions, branches and loops as much as you like but take care. It is easy to make mistakes with lots of indents. Splitting things up into helper functions is makes the code much easier to manage.

### Practice combining functions, branches and loops

Go back to quiz game you started in the [section about branches](#practice-with-branches). Change your programme by mixing in functions and loops and some new branches. Add these features and make sure they work before trying the next one. Remember to use small helper functions to keep your blocks of code small and easy to understand:

- Put the questions and answers into lists and turn the quiz into a loop. There are several ways to do this but here is a hint

    ```python
    quiz=[ # A list of tuples
        ('question1','answer1'), 
        ('question2','answer2'),
        ...
    ]
    for (q,a) in quiz:
        ... # q will be each question in turn
        ... # a will be the matching answer each time 
    ```

- allow the quiz player to pass if they don't know the answer
- give a penalty score (e.g. lose 5 points) if they get an answer wrong. There is no penalty for passing.
- set a limit to the number of passes (e.g. 3 times each quiz)
- If the player has used up their passes but tries to pass again print an appropriate message and ask the question again.
- Put the whole quiz inside a loop and at the end of each quiz invite another player to try.
- Keep a track of the highest score so far.
- If a player beats the high score let them enter a gamer tag (such as 3 letters).
- Print the top few high score before each quiz starts. Here are some hints that you might use.

    ```python
    high_to_low = [] #empty high score tables
    low_to_high = []
    high_to_low.insert(0,(500,'AAA')) # put a new high score at the beginning
    highest_score = high_to_low[0]
    low_to_high.append((500, 'AAA')) # add a new high score at the end
    highest_score = low_to_high[-1]
    ```

- Read the questions and answers from a text file. You might need some help about [looping through a file](https://www.w3schools.com/python/python_file_open.asp#:~:text=By%20looping)
- If a player beats the highest score also let them add a new quiz question and answer. You might need to close and open the quiz file in a different mode.

## Even more practice

There are loads of online places to get more practice but please check with a responsible adult to make sure you meet any age limits and get permission for anything that has a cost. [Codewars (14+ years)](https://codewars.com) offers free challenges and lets you earn points and badges as you progress.
