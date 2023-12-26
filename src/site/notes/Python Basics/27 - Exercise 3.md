---
{"dg-publish":true,"permalink":"/python-basics/27-exercise-3/","dgPassFrontmatter":true,"noteIcon":"1","created":"2023-12-25T20:31:18.781+05:30","updated":"2023-12-26T13:46:43.477+05:30"}
---

🧶 Tags:: #Python_Basics 
Up:: [[Python Basics/28 - F Strings\|28 - F Strings]]
Down:: [[Python Basics/25 - Operations on Tuples\|25 - Operations on Tuples]]
🗃 Resources:: [Playlist](https://www.youtube.com/playlist?list=PLu0W_9lII9agwh1XjRt242xIpHhPT2llg)
==2023-12-25 - 20:31==

Create a program capable of displaying questions to the user like KBC. Use List data type to store the questions and their correct answers. Display the final amount the person is taking home after playing the game.

```python
# Define questions and answers using tuples
questions = (
    ("What is the capital of France?", "A. Paris", "B. London", "C. Berlin", "D. Madrid", "A"),
    ("Which planet is known as the Red Planet?", "A. Venus", "B. Mars", "C. Jupiter", "D. Saturn", "B"),
    # Add more questions in a similar manner
)

def play_game(questions):
    total_questions = len(questions)
    winnings = 0

    for i, (question, option_a, option_b, option_c, option_d, correct_answer) in enumerate(questions, start=1):
        print(f"\nQuestion {i}:")
        print(question)
        print(option_a)
        print(option_b)
        print(option_c)
        print(option_d)

        user_answer = input("Enter your choice (A/B/C/D): ").upper()

        if user_answer == correct_answer:
            print("Correct!")
            winnings += 100000  # Add prize money for correct answer
        else:
            print(f"Wrong! The correct answer was {correct_answer}.")
            break  # End game if the answer is wrong

    print(f"\nGame Over! You won ${winnings}.")

# Start the game
play_game(questions)
```

This was harder that it looked so, I took help from ChatGPT to get this.