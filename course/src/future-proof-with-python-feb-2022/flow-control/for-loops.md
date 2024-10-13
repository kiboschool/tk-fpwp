# For loops

*Estimated Time: 20 minutes*

---

We often want code to run again and again, until it’s time to stop. We learned that a `while` loop is a great tool when you know the stopping condition.

In this section we will explore a second tool for repeating code: the `for` loop. A `for` loop is a good fit when we want to run a block of code a definite number of times, or when we want to iterate over list of things.

# `for` Loops

`for` loops step through a list of items in order. Each iteration will assign the next item to the loop variable, then execute the loop body.

The syntax of a `for` loop is similar to a `while` loop. It starts with the `for` keyword, and has an indented loop body. Instead of a condition, a `for` loop has a variable name, the `in` keyword, and a list of things to loop through.

```python
for variable in items:
	loop body to execute
```

The flow chart of a `for` loop is:

![2%204%20for%20Loops%20f805c25670624ae7b6ef78e858f763d5/Untitled.png](/future-proof-with-python-feb-2022/working-with-data/variables-and-assignment/untitled.png)

## Comparing `while` and `for`

Let's take a look at an example of a  `for` loop:

```python
for i in [5, 4, 3, 2, 1] :
	print(i)
print('Blastoff!')
```

This `for` loop will have the same output as the `while` loop we saw earlier:

```
5
4
3
2
1
Blastoff!
```

Let’s compare the `for` loop side by side with the `while` loop :

```python
for i in [5, 4, 3, 2, 1] :
	print(i)
print('Blastoff!')
```

```python
n = 5
while n > 0:
    print(n)
    n = n - 1
print('Blastoff!')
```

<aside>


🤔 Compare the two code examples above (the `for` loop  and the `while` loop). What do you notice about them?

- `while` vs. `for`
    
    Similarities:
    
    - loop keyword, then something, then `:`
    - loop body is indented
    
    Differences:
    
    - variable `n` created before the loop, variable `i` created as part of the `for` statement
    - `while` loop changes the variable with `n = n - 1`, `for` loop variable changes automatically
    - `for` loop has to write out exactly what numbers the iteration variable will have
    
</aside>

## `for` loop iteration variable

The initial statement in the `for` loop is:

```python
for i in [5,4,3,2,1]:
```

In this code, the loop creates a new variable `i`. Its value will change in each iteration of the loop, to take on the value of each item in the list. In this example, `i` will take on successive values of 5, 4, 3, 2, and 1.

As you can see, `for` loops offer a more direct syntax than `while` loops, because you can explicitly declare the values of the iteration variable.

We’ll cover the list syntax `[5, 4, 3, 2, 1]` in more detail later in the course. For now, you can use it to write `for` loops, without knowing exactly what it means. You can put any values inside the `[]`, and the loop variable will be assigned to each value in turn.

## Practice

<aside>


👩🏿‍💻 Write a `for` loop that displays Hello, plus each name in the list.

- The output should be like this screenshot
    
    ![2%204%20for%20Loops%20f805c25670624ae7b6ef78e858f763d5/Untitled%201.png](/future-proof-with-python-feb-2022/flow-control/multi-way-decisions/untitled-1.png)
    
</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://replit.com/team/fpwp-feb2022/W25-For-Loop-Practice" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

## Range function

There’s another way to tell the `for` loop what values to iterate over. `range()` is a function that generates a series of numbers within a certain range.

```python
# Same loop as before, using range()
for i in range(5,0,-1):
	print(i)
print("Blastoff!")
```

```
5
4
3
2
1
Blastoff!
```

For longer lists of numbers, `range` is easier than typing the whole thing out.

The syntax for the range function is below.

```python
range(start, stop, step)
```

- ***start*** specifies the first value of the range.
- ***stop*** specifies the stopping point.
    - The stop value is **not** included in the range, so `range(1,10)` will only go up to `9`.
- ***step*** specifies how much to count by each time. `range(2,10, 2)` produces `2`, `4`, `6`, `8`.
    - The **default value** is 1, which means that if you leave *step* out, `range` will count by 1.

Here’s some examples using `range`:

```python
# Print the numbers 1-10 
for n in range(1,11): # 11 is not included!
	print(n)

# Print the numbers 5, 10, 15, 20... 100, counting by 5s
for number in range(5, 101, 5):
	print(number)

# Print the numbers counting down from 5 to 1
for i in range(5,0,-1):
	print(i)
print("Blastoff!")
```

## Range Practice

<aside>


🎯 Practice writing `for` loops that use `range`.

- Print the numbers from 4 to 14
- Print the numbers from -10 to 10
- Print the numbers from 1 to 20, counting by 2s
- Print the numbers from 1000 to 500, counting backwards by 100s
</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://replit.com/team/fpwp-feb2022/W26-Range-Practice" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

---

<aside>


<img src="../man-in-hike.png" alt="../man-in-hike.png" width="40px" /> Next up: [Practice](/future-proof-with-python-feb-2022/flow-control/practice-loops-and-conditionals.md)

</aside>