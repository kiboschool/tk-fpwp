# Loop patterns

*Estimated Time: 40 minutes*

---

You’ve learned and practiced some of the core actions of working with lists. You can create a list, add and remove items, and perform actions for all of the items. Now it’s time to learn to write code that uses lists and loops to solve problems.

Using lists and loops together, you can answer questions about data.

- *What’s the smallest (or largest) item in this list?*
- *What’s the sum of all the items in the list? What’s the average?*
- *What are the items in the list that fit this condition?*

When solving more complicated problems with lists, it’s also helpful to have more powerful debugging techniques. In this lesson, you’ll learn problem solving with loops, including common patterns and strategies for figuring things out.

## Video: Lists and Loops

<aside>


<img src="../instruction.png" alt="../instruction.png" width="40px" /> Watch this video to learn about lists and loops.

</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.loom.com/embed/f1a3374792a54c378b710954bf5a2a0d" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## Looping through a list with `for`

When you first saw the `for` loop, you learned that it could loop through a list, or through a `range`. You’ve been using this the whole time, but as a quick refresher, here’s a loop that will print the numbers from 5 down to 1:

```python
for number in [5,4,3,2,1]:
	print(number)
```

And here’s another version, using `range`:

```python
for number in range(5,0,-1): # start at 5, go down to (but not including) 0, by -1 each time
	print(number)
```

We’ll be using `for` loops for almost all of the loop and list problems here. A `while` loop can work in some circumstances, but it’s usually a little more work.

### Sum of numbers in a list

Here’s a python program to add up all the numbers between 1 and 10:

```python
total = 0
for number in [1,2,3,4,5,6,7,8,9,10]:
	total += number
 
print(total) # 55
```

Here’s what this program does:

- **Step 1:** Creates a variable called `total`, which starts at `0`
- **Step 2:** Loop through the numbers 1 through 10. Increase `total` by the `number` each time.
- **Step 3:** After the loop, print out the total

<aside>


⚠️ **Common Mistake:** If you create a variable inside the loop*,* it will get re-created from scratch each time the loop body executes.
To make sure you are updating the variable every iteration, you have to **create the variable before the loop.**

- Here is the wrong version. `total` is created inside the loop, so it doesn’t work. **Don’t do this!**
    
    ```python
    for number in range(1,11):
         total = 0          # total gets re-assigned 0 every time the loop body runs
         total += number
    
    print(total) # 10   <- WRONG!
    ```
    
</aside>

## Solving problems using loops

Many loop problems can be solved using the pattern in this example: **update the variable every time you go through the loop.** In this lesson, you’ll see lots of different problems you can solve with this pattern. 

<aside>


🔑 **Common pattern**

**Step 1:** Create a variable before the loop starts and set the initial value.

**Step 2:** Perform some computation on each item in the loop body, which may change the value of the variable.

**Step 3:** Use the value of the variable when the loop completes.

</aside>

Let’s try it out.

## Practice

<aside>


🔢 Find the sum of the **even** numbers from 10 to 100 (including 10 and 100).

*Remember, you can use the third argument to* `range` *to control the step size.*

</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://replit.com/team/fpwp-feb2022/W33-Sum-of-Range" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

- Solution (try for 5 minutes before peeking)
    
    ```python
    total = 0
    # We want to include 100, so we stop at 101
    # We want even numbers, so step by 2
    for i in range(10,101,2): 
      total+=i
    print(total)
    ```
    

## Loop debugging: Printing each step

Usually it takes more than one try to write the code to solve a problem with loops. When the code isn’t working correctly, you need a strategy for figuring out what is happening, and fixing it.

**Printing values each step** is a strategy for debugging what’s happening in your loop. Let’s see what it looks like.

Here’s some broken code for solving a loop problem:

```python
# Find the total of the even numbers from 2 to 12
total = 0
for i in range(1,12,2):
	total + i
print(total) # 0  <- Wrong, should not be 0!
```

You might be able to spot the bug in this code, but let’s try printing out the values to debug it. 

```python
total = 0
print("before the loop total is", total) # Added
for i in range(1,12,2):
	print("i is", i, "total is", total) # Added
	total + i
print("after the loop total is", total) # Added
print(total)
```

Here’s the output:

```
before the loop total is 0
i is 1 total is 0
i is 3 total is 0
i is 5 total is 0
i is 7 total is 0
i is 9 total is 0
i is 11 total is 0
after the loop total is 0
0
```

Wow! It looks like there are actually 3 bugs!

- instead of the even numbers, `i` is getting set to the odd numbers
- instead of including `12`, it’s stopping at `11`
- `total` isn’t changing at all in the loop

### Fixing the code

Since we can see the values, it’s much easier to tell what we need to fix.

- `range` needs to start at `2` (instead of `1`)
- `range` needs to stop at `13` (instead of `12`)
- it needs to be `total += i` instead of `total + i`

When we fix the code, we can leave the `print`s in to make sure our changes work.

```python
total = 0
print("before the loop total is", total)
for i in range(2,13,2):
	print("i is", i, "total is", total)
	total += i
print("after the loop total is", total)
print(total)
```

Now the output is:

```
before the loop total is 0
i is 2 total is 0
i is 4 total is 2
i is 6 total is 6
i is 8 total is 12
i is 10 total is 20
i is 12 total is 30
after the loop total is 42
42
```

Now that we can see that the code is working, we can remove the extra `print` statements. Here’s the final code:

```python
total = 0
for i in range(2,13,2):
	total += i
print(total)
```

## Practice

<aside>


🐛 Practice using `print` to debug a faulty loop.

</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://replit.com/team/fpwp-feb2022/Loop-Debugging-With-Print" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

- Solution (try for 5 minutes before looking)
    
    ```python
    total = 0
    print("total before is", total)
    for i in range(10,25,2):
      print("i is", i, "total is", total)
      total + i
    print("total after is", total)
    print(total)
    
    # BUGS
    # - supposed to be the odd numbers (range should start at 11)
    # - supposed to include 25 (range should end at 26)
    # - should be total += i
    ```
    

# Conditions and Lists

<aside>


<img src="../instruction.png" alt="../instruction.png" width="40px" /> Watch this video to learn about lists and loops with conditions.

</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.loom.com/embed/b567c2661782431a86891fcc9337d3d3" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## Check if an item is in the list

Sometimes you want to find out if some item is in the list. You can use the same pattern as before, but with a different change to the variable in the loop body.

Here’s an example:

```python
# Does the list have string "Python" in it?
languages = ["Ruby", "JavaScript", "C", "Rust", "Smalltalk", "Clojure", "Python"]

has_match = False
for language in languages:
	if language == "Python":
		has_match = True

print(has_match)
```

It’s the same pattern as before, but with an `if` statement in Step 2.

- 🔑 **Step 1:** Create a variable called `has_match`, which starts as `False`
- 🔑 **Step 2:** Loop through the strings in the list. If the string matches, set `has_match` to `True`
- 🔑 **Step 3:** Print out the `has_match` variable

<aside>


⚠️ Note: You could use the `in` operator for this problem.

- `in` is easier if we want to check for a specific item.
- Using a loop makes it possible to check more complicated conditions like *“Is there a string in this list longer than 40 characters?”*
</aside>

## Loop debugging: Visual Tracing

When debugging more complicated code, it’s helpful to be able to see how the code executes step by step. You can use [pythontutor.com](https://pythontutor.com/visualize.html#mode=display) to run your code step by step, and see the values of all your variables as the program runs.

Here’s the [**example from before in pythontutor**](https://pythontutor.com/visualize.html#code=%23%20Does%20the%20list%20have%20string%20%22Python%22%20in%20it%3F%0Alanguages%20%3D%20%5B%22Ruby%22,%20%22JavaScript%22,%20%22C%22,%20%22Rust%22,%20%22Smalltalk%22,%20%22Clojure%22,%20%22Python%22%5D%0A%0Ahas_match%20%3D%20False%0Afor%20language%20in%20languages%3A%0A%20%20%20%20if%20language%20%3D%3D%20%22Python%22%3A%0A%20%20%20%20%20%20%20%20has_match%20%3D%20True%0A%0Aprint%28has_match%29&cumulative=false&curInstr=0&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false)

<aside>


🎥 Watch this video to see how to step through the code using PythonTutor

- **How to use PythonTutor to step through your code**
    
    <div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.loom.com/embed/6d7c8dad5058464c8c968fbcd931ec2e" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
    
</aside>

Similar to printing out the values at each step, PythonTutor helps you see what’s happening when your code runs. That makes it easier to spot bugs.

## Filter a list

Sometimes, you want to find only the values in your list that meet a certain condition.

Again, we can use the three step pattern. The variable we are updating will be a new list, with just the filtered values.

```python
numbers = [62, 60, 53, 53, 33, 3, 25, 61, 36, 1, 69, 55, 56, 39, 32, 76, 20, 62, 47]
# Write a program to find all the even numbers in the list
evens = []
for element in numbers:
  if element % 2 == 0:
		evens.append(element)

print(evens) # [62, 60, 36, 56, 32, 76, 20, 62]
```

We use an `if` statement and the modulo operator to find the even values, and add them to the list.

## Practice

<aside>


👩🏿‍💻 Write a loop that finds the total of all the odd numbers in the list.

</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://replit.com/team/fpwp-feb2022/W35-Sum-of-Odd-Numbers" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

- Solution (try for at least 5 minutes before looking)
    
    ```python
    numbers = [62, 60, 53, 53, 33, 3, 25, 61, 36, 1, 69, 55, 56, 39, 32, 76, 20, 62, 47]
    
    total = 0
    for n in numbers:
      if n % 2 == 1:
        total += n
    
    print(total)
    ```
    

## Smallest Item

Finding the minimum value in a list uses the same pattern. Step through the elements of the list, and update a variable that is tracking the *current* minimum value.

Each time through the loop, check if the number is smaller than the current minimum value. If it is, then it’s the new minimum value.

We can use the first value in the list as the initial value of the minimum.

```python
numbers =  [62, 60, -53, 53, 33, -3, 25, 81, 36, 1, 69, 55, 56, 39, -32, -76, 20, 62, 47]
minimum = numbers[0]
for number in numbers:
	if number < minimum:
		minimum = number

print(minimum) # -76
```

With one small change, this same code works to find the largest value instead.

## Practice

<aside>


👩🏿‍💻 Follow the prompts in the comments to write a program to find the smallest number among numbers the user enters.

The program should look like this when it runs:

![enter.png](/future-proof-with-python-feb-2022/loops-and-lists/loop-patterns/enter.png)

</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://replit.com/team/fpwp-feb2022/W36-Interactive-Minimum" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

- **Interactive Minimum: Solution**
    
    ```python
    numbers = int(input("How many numbers will you enter? "))
    i = 0
    minimum = float('inf')
    
    for i in range(numbers):
      x = int(input("Enter a number: "))
      # check whether x is smaller than minimum, and reassign minimum to it if so
      if x < minimum:
        minimum = x
    
    print("The smallest number is:", minimum)
    ```
    

---

<aside>


<img src="../man-in-hike.png" alt="../man-in-hike.png" width="40px" /> Next up: [Practice](/future-proof-with-python-feb-2022/loops-and-lists/practice-lists-and-loops.md)

</aside>