# Building our own functions

*Estimated Time: 40 minutes*

---

In this section, we investigate creating new functions. 

<aside>


🧑🏿‍🍳 A function is like a recipe. It has ingredients, steps to follow, and if all goes to plan, there’s a ‘meal’ that it produces. So far, your programs have used recipes from Python’s “recipe book” — built-in functions. Now, you’ll see how to write your own recipes, and tell Python to follow them step by step.

</aside>

## Video: Functions in Python

<aside>


<img src="../instruction.png" alt="../instruction.png" width="40px" /> Watch this video to learn about functions.

</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.loom.com/embed/584390ac33ac47e096bc92d693a84cc0" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

### Defining a function

We use the keyword `def` (short for ‘define’) to create a new function. When you define a function, you specify a *name* for the function as well as a sequence of statements in an indented block. The function is stored in the program’s memory, but the code does not run right away. After the definition, we can *call* the function to run the code.

Here’s what it looks like:

```python
# Define a function.
def function_name(parameter_1, parameter_2):
	# Follow these steps (the indented function body)
	# print each parameter
	print(parameter_1)
	print(parameter_2)

# Use function_name to call the function.
function_name(argument_1, argument_2)
```

When defining a function:

- Use the keyword `def`
- Give the function a name, ideally one that tells what the function does
- Give names for each of the function's parameters
- Use an indented block for the code for the function

Below is an example of a Python function that calculates the sum of two numbers:

```python
def add(a, b):
  return a + b
```

Later, when we want to run the statements in the function, we can call the function, which will then run all of its statements.

```python
add(3, 5) # 8
add(10, 30) # 40
```

## Parameters and Arguments

```python
def add(a, b):
  return a + b
```

In the example above, `a` and `b` are **parameters**. Parameters are names that stand in for the values passed to the function. You use them in the function body like variables.

We can call the add function like this:

```python
>>> add(3,5)
8
```

The values passed to the function are called **arguments**. In this example, `3` and `5` are arguments. The parameters `a` and `b` get assigned the values `3` and `5` in the function body.

<aside>


🤷🏿‍♂️ An **argument** is a value provided to a function when the function is called.
A **parameter** is a named spot in a function definition, where the argument will go.

Parameters **and arguments **are similar concepts. Parameters are in the definition, arguments are when you actually call the function. It’s not super important that you memorize which is which. A lot of programmers use the terms interchangeably.

</aside>

## Practice

<aside>


👩🏿‍💻 Write a function called **greet** which will print out three lines of personalized greeting. The function should take as its argument a name then print the messages below. Modify the starter code below.

</aside>

A sample run of your code with argument Keno, i.e., `greet("Keno")` should look like this:

![4%202%20Building%20Our%20Own%20Functions%20baf32b0ffc134773b0d51bf7b17cda3c/Untitled.png](/future-proof-with-python-feb-2022/working-with-data/variables-and-assignment/untitled.png)

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://replit.com/team/fpwp-feb2022/Greet-Person-Function" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

<aside>


🤔 Modify the code above to put the function definition at the end of the program. What do you notice happens? Try it first then click below for the explanation.

- Explanation
    
    If you put the function definition at the end of the program, you will get an error. A function must be defined before you use it in your program. If you write greet(Keno) first, Python doesn't know this function and will error. We must define functions at the beginning of our programs before we use them. **There is a way however to get around this (call a function that its definition comes later in the file) but it is out of our discussion scope now)**. 
    
</aside>

## Return Values

Often, a function will take its arguments, do some computation, then return a value to be used where the function was called. The `return` keyword is used for this. In our example, the statement `return a + b` is called the *return statement*. It ends the function execution and sends back `a + b` which is the result of the function. 

It is common to say that a function “takes” arguments and “returns” a result.

Note that some functions do not necessarily return a result. 

You can visualize a function as a machine that takes in arguments, and spits out the return value:

![Untitled](/future-proof-with-python-feb-2022/flow-control/multi-way-decisions/untitled-1.png)

Concretely, for the `add` function that we defined and called like this:

```python
def add(a,b):
	return a + b

add(3,5)
```

![Untitled](/future-proof-with-python-feb-2022/flow-control/multi-way-decisions/untitled-2.png)

Programs can use the return value for further operations:

```python
result = add(3,5)
print("the result was", result) # the result was 8
bigger_result = add(result, 10)
print("the bigger result was", bigger_result) # the bigger result was 18
```

## Return vs. Print

`print` is different from returning a value. If you use `print`, a message shows up in the console, but the rest of the program doesn’t get to see it.

```python
def add_and_print(a,b):
	print(a + b)

result = add_and_print(3,5) # 8 
print("the result was", result) # the result was None
```

The `print` in the function will print out the value, but it will not return it. `None` is the value that functions return by default. If they don’t return something else, they return `None`.

![Untitled](/future-proof-with-python-feb-2022/flow-control/assignment/untitled-3.png)

<aside>


⚠️ `print` is different from `return`. So far in the course, you’ve used `print` to see results, so you are used to using lots of `print`. In more complicated programs, `return` is used more often.

Most of the practice exercises will require you to use `return`, not `print`

</aside>

## Practice

<aside>


👩🏿‍💻 Write two functions. The first, called `print_double`, should print out a number times two. The second, `return_double`, should return two times the argument instead of printing. 

Run the code to see the results.

</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://replit.com/team/fpwp-feb2022/W42-Double-Doubles" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## Functions can have any code inside

Any code can go inside a function. Variables, loops, conditions, other function calls — it all works. Anything that you’ve written in a program so far can go inside a function.

```python
# A function with an if/else statement
def check_password(attempt):
	password = "sEcRetPaSsWoRd"
	if attempt = password:
		return "You're in!"
	else:
		return "Access denied"

print(check_password("open sesame")) # Access denied
print(check_password("sEcRetPaSsWoRd")) # You're in!

# A function with a loop inside
def add_up_to(number):
	total = 0
	for i in range(1,number):
		total += number
	return total

print(add_up_to(5))   # 20
print(add_up_to(10))  # 90
print(add_up_to(100)) # 9900
```

<aside>


⚠️ **Indentation**
Make sure you get the indentation right. Indent one more level for each block some code is inside of. So, if some code is inside a condition, and the conditional is inside a function, the code in the conditional is indented 2 times.

```python
# Showing the indentation with ->
def check_password(attempt):
->password = "sEcRetPaSsWoRd"
->if attempt = password:
->->return "You're in!"
```

</aside>

## Types of return values

Functions return different types of values. Here is an example of a  function that checks if a given username is valid or not. It returns a boolean:

```python
def is_valid(username):
  if len(username) > 5:  #checks to see if username has more than 6 characters
    return True
  else: 
    return False

print(is_valid('user'))    # will print False
print(is_valid('mhassan')) # will print True
```

You can return any of the types you’ve learned so far from a function.

<aside>


<img src="../man-in-hike.png" alt="../man-in-hike.png" width="40px" /> Next up: [Practice](/future-proof-with-python-feb-2022/functions/practice.md)

</aside>