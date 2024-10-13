# Modules

In Python, **modules** are files that contain code that's ready for us to use. 

Here are a few examples:

- The `random` module that we previously used to generate random numbers.
- The `cmath` module offers complex mathematical functionality.
- The `csv` module is for reading and writing tabular data to and from delimited files.
- The `email` module supports *parsing, manipulating, and generating email messages.*
- The `scikit-learn` library contains modules for machine learning work.

There are tons of modules and libraries out there. When you need to implement some feature and you don't know how, you can search for a module that provides these functions for you.

## Importing Modules

To use a module, you’ll need to `import` it using Python’s module system. You’ve used `import` before, for code like this:

```python
import random
random_number = random.randint(0, 100)
print(random_number) # 76 (when I ran it - different each time)
```

`random` is a **module** with useful functions like `randint`, which generates a random number. Modules are python’s way of grouping related functions.

### What functions does a module provide?

To find the functions that a module provides, you can use Google, or look at the documentation (”docs”) for that module.

[https://docs.python.org/3/library/random.html#module-random](https://docs.python.org/3/library/random.html#module-random) is the link to the docs for the `random` module. Click it to see everything there is to know about `random`. 

<aside>


📖 Tips for Reading Documentation

- Documentation covers *everything.* You probably only need a small part - skim, search, and scan to find what you actually need
- Function descriptions look like this:
    
    > **random.choice(*seq*)**
    > 
    > 
    > Return a random element from the non-empty sequence *seq*. If *seq* is empty, raises `[IndexError](https://docs.python.org/3/library/exceptions.html#IndexError)`.
    > 
    
    This one means you can pass a sequence (like a list) into the `choice` function provided by the `random` module, and it will return a random element from the list.
    
- Sometimes it’s helpful to just see the name of a function, then go try it out to see what it does.
</aside>

### What modules are available?

You can use Google to find a Python module, or look at the [index of all built-in modules](https://docs.python.org/3/py-modindex.html). There’s a lot of modules, so you might scan it now, then just Google it when there’s something in particular that you need.

Lots of modules are not built into python — they’re written by other developers. In order to use modules that aren’t built in, you need to install them so that they are available to `import`. In Replit, you can use the package manager button on the left panel to search for modules to install.

## Modules you’ll use

In the “Distance Traveled” Practice below, you’ll need to import the `math` module to use the `math.sqrt` function. In "Quick Draw” Practice, you will need to import the `random` module to generate random numbers, and you’ll need the `time` module to measure how long things take. 

In the past, students have used modules for special features in their final projects, such as:

- the `requests` module to interact with data over the web
- the `gtts` module for text-to-speech
- the `termcolor` module to change the color of the text output
- various modules for drawing images and figures

## Practice: Distance Traveled

<aside>


⚽ In this assignment, you'll calculate the distance a football player traveled in a game.

**Access** and **submit** the assignment in Replit here: <div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://replit.com/team/fpwp-feb2022/P47-Distance-Traveled" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

</aside>

<aside>


<img src="../instruction.png" alt="../instruction.png" width="40px" /> Watch the video below to see the full solution

- **Distance Traveled: Solution**
</aside>

## Practice: Quick Draw

<aside>


👩🏿‍💻 In this assignment, you'll use the `random` and `time` modules to help you create a game that tests your reaction time. There's no unit tests for this one, so you'll have to run the program to check whether or not you've got it working right!

**Access** and **submit** the assignment in Replit here: <div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://replit.com/team/fpwp-feb2022/P48-Quick-Draw" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

</aside>

<aside>


<img src="../instruction.png" alt="../instruction.png" width="40px" /> Watch the video below to see the full solution

- **Quick Draw Solution**
    
    <div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.loom.com/embed/2952347e63a1497b982df66218870052" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
    
</aside>

---

<aside>


<img src="../man-in-hike.png" alt="../man-in-hike.png" width="40px" /> Next up: [Assignment](/future-proof-with-python-feb-2022/functions/assignment-optional.md)

</aside>