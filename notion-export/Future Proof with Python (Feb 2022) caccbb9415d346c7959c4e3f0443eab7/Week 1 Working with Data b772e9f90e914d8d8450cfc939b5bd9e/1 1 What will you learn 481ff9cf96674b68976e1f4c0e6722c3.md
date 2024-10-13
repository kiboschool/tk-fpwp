# 1.1. What will you learn?

*Estimated time: 10 minutes*

---

## Skills

In the next few weeks, you’ll learn to make programs that can:

- Get input from the user, and show them messages
- Work with numbers and text
- Make decisions
- Repeat operations over again
- Work with lists of data

<aside>
⚠️ **Reminder.** For an overview of lessons and the weekly schedule, see:

</aside>

## Final Project Example

At the end of the course, you’ll make a final project of your own design, using the skills you learn in the program.

Here’s a **Guess the Capital** project by a past student that shows the different concepts you’ll learn. (*Press the green button to play the game*).

<aside>
🤔 You don’t need to understand this code yet. Each week, you’ll learn more about how these work in detail. But, for now, you can just have fun with the project and get a sense of what will come later.

</aside>

[https://replit.com/@kibocurriculum/Final-Project-Sample-FPWP#main.py](https://replit.com/@kibocurriculum/Final-Project-Sample-FPWP#main.py)

In the project code, you can see each of the concepts you’ll learn over the next few weeks. 

<aside>
<img src="../instruction.png" alt="../instruction.png" width="40px" /> *Open the toggles to show snippets where the concept is used in the project above.*

</aside>

- **Data**: strings, numbers, booleans, and variables
    
    ```python
    # Strings, Numbers, Variables, and Booleans
    print("Welcome to GUESS THE CAPITAL")
    score = 0
    final_score > 50 and final_score < 70
    
    ```
    
- **Operators:** using `+` , `*`, `=`, and other symbols to do calculations and operations
    
    ```python
    option_labels[index] + ". " + capitals[option]
    score += ask_question(country)
    score * 10
    final_score > 50
    
    ```
    
- **Input and Output:** (`input` and `print`)
    
    ```python
    print("PERFECT SCORE! You are AWESOME!!")
    user_answer = input("Answer: ").upper()
    ```
    
- **Flow Control**: Conditional statements and Loops
    
    ```python
    for index in range(4):
        option = random_options[index]
        print(option_labels[index] + ". " + capitals[option])
    
      user_answer = input("Answer: ").upper()
      if user_answer in option_labels:
        answer_index = option_labels.index(user_answer)
    
        if random_options[answer_index] == country:
          return 1
    ```
    
- **Lists:** storing and operating on lots of pieces of data
    
    ```python
    countries = ["Indonesia", "Malaysia", "Austria", "Cameroon", "Colombia", "Jamaica", "Morocco", "Bolivia", "Canada", "Belgium", "Spain", "Australia", "Poland", "Chile", "Egypt", "Ghana", "Argentina", "Croatia", "Brazil", "France"]
    ```
    
- **Functions**: built-in functions, and user-defined functions
    
    ```python
    user_input.upper()
    random.sample(range(33), 4)
    
    def show_score(final_score):
      print (f"Your final score is {final_score}%")
    ```
    

In week 1, you’ll learn the basics: **data**, **variables**, **operators**, **input** and **output**. 

In week 2, you’ll learn flow control with **conditions** and **loops**

In week 3, you’ll learn about storing data in **lists** and do more practice with **loops**

In week 4, you’ll learn about **functions**.

## Mindset

Along the way, your mindset will change.

- You’ll be less scared about computers and **more confident** 💪🏿
- You’ll know **how to debug** and find a solution when things don’t work 🐛
- You’ll make friends and **collaborate with teammates** 👥
- You’ll learn how to **break problems down** into smaller pieces and solve them piece by piece 🧩

Let’s hear from some Kibo alumni about their learning journey.

- **Alexis** (Try Kibo Alum)
    
    [https://www.youtube.com/watch?v=nlYn1qDSdek](https://www.youtube.com/watch?v=nlYn1qDSdek)
    
- **Ayo** (Try Kibo Alum)
    
    [https://www.youtube.com/watch?v=KI3HZ8DhuII](https://www.youtube.com/watch?v=KI3HZ8DhuII)
    

<aside>
<img src="../man-in-hike.png" alt="../man-in-hike.png" width="40px" /> Next up: [Programs and Comments](1%202%20Programs%20and%20Comments%207b56dd514edc4005acb3fe712d507e06.md)

</aside>