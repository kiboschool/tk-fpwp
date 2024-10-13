# Assignment

*Estimated time: 2 hours*

---

# Individual Project: Rock Paper Scissors

**Due date: Sunday Feb 20**

<aside>


📌 This is an individual project. You are expected to work independently.

If you get stuck, confused, or have trouble with the project, you should use the **#help-python** channel in Discord or message an instructor. Try not to spoil the project for others - use Discord spoiler tags if you are going to include a screenshot or code sample.

</aside>

<aside>


✂️ **Access** and **submit** the assignment in Replit here: <div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://replit.com/team/fpwp-feb2022/Assignment-2-Rock-Paper-Scissors" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>

</aside>

## Rock, Paper, Scissors

In this assignment, you'll recreate the classic game of rock, paper, scissors. If you’ve never played before, or need a refresher: two players each choose Rock, Paper, or Scissors. They show their choice at the same time. Depending on their choice, there’s a win, lose, or draw.

- Rock smashes Scissors
- Scissors cut Paper
- Paper covers Rock
- if the two choices are the same, it’s a draw
- Rock, Paper, and Scissors are the only choices allowed.

## How to get started

Here are the basic steps:

- Set a value for the computer player
- Get user input for Rock, Paper, or Scissors
- Use `if` statements to print the right message, based on the computer and player choices
- There are a lot of `if` statements to write.
- Be aware that the user might not type in exactly “Rock” “Paper” or “Scissors”. Your code should handle that case nicely, and should not error.

**Sample Runs at this stage**

![Untitled](/future-proof-with-python-feb-2022/working-with-data/variables-and-assignment/untitled.png)

![Untitled](/future-proof-with-python-feb-2022/flow-control/multi-way-decisions/untitled-1.png)

![Untitled](/future-proof-with-python-feb-2022/flow-control/multi-way-decisions/untitled-2.png)

![Untitled](/future-proof-with-python-feb-2022/flow-control/assignment/untitled-3.png)

<aside>


🛑 **Stop**
Before you move on, try playing your game, and make sure that it’s working for all the different inputs. It’s not fun if the conditionals don’t work, because it feels like the game is broken.

You should click “Submit” when your project is working at this stage, and then continue working on the next part.

</aside>

## What to do next

- Use `random` to randomize the computer choice. The computer player should choose randomly between Rock, Paper, and Scissors.
- Use a loop to play multiple rounds.
    - Instead of stopping after just one round, it should be first to three wins.
    - Keep track of the number of wins for the user and the computer player.
    - Stop the loop as soon as either the computer or human player has won 3 times.
- Check that your game works by playing it and testing it.

<aside>


🪨 **Full gameplay example**

Compare your program's output to the screenshots. Does your program work the same?

- Expand to show **screenshot**
    
    ![Untitled](/future-proof-with-python-feb-2022/flow-control/assignment/untitled-4.png)
    
- Expand to show **text transcript**
    
    ```
    Welcome to rock, paper, scissors. Let's play first to three wins.
    
    You have won 0 times. The computer has won 0 times.
    Rock, Paper, or Scissors? Paper
    The computer chooses Rock
    Paper covers Rock. You win!
    
    You have won 1 times. The computer has won 0 times.
    Rock, Paper, or Scissors? Scissors
    The computer chooses Rock
    Rock smashes Scissors. You lose!
    
    You have won 1 times. The computer has won 1 times.
    Rock, Paper, or Scissors? Rock
    The computer chooses Rock
    It's a draw
    
    You have won 1 times. The computer has won 1 times.
    Rock, Paper, or Scissors? Paper
    The computer chooses Scissors
    Scissors cut Paper. You lose!
    
    You have won 1 times. The computer has won 2 times.
    Rock, Paper, or Scissors? Paper
    The computer chooses Rock
    Paper covers Rock. You win!
    
    You have won 2 times. The computer has won 2 times.
    Rock, Paper, or Scissors? Paper
    The computer chooses Rock
    Paper covers Rock. You win!
    
    Nice work, you were the first to win three rounds!
    ```
    
</aside>

If your Rock Paper Scissors game is working, with “first to three” with a randomized computer player, you can add additional features that you come up with. Be sure that the basic version still works!

## Rubric

There aren't any test cases for this assignment. Instead, you'll have to check that it works for yourself.

**Basic Gameplay**

- [ ]  The program prints out instructions for the user
- [ ]  The program runs without errors, even if the user types in the wrong thing
- [ ]  The program prints out the right messages, based on the choices the user and computer player made

If you checked off all these boxes, your Rock, Paper, Scissors game is working!

**Gameplay with loops**

- [ ]  The program plays the game for multiple rounds
- [ ]  The program shows the score after each round
- [ ]  The program ends after the player or computer win three times

If you checked off these boxes, then your extended game is working!

## Remember...

- **Plan** before you code
- **Debug** if you aren't getting the desired output
- **Attend** office hours if you need additional support
- **G**o **C**limb **K**ibo!

---

<aside>


<img src="../man-in-hike.png" alt="../man-in-hike.png" width="40px" /> Next up: [Wrap Up](/future-proof-with-python-feb-2022/flow-control/wrap-up.md)

</aside>