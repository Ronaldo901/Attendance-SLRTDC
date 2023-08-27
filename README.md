def ask_question(question, options, answer):
    print(question)
    for i, option in enumerate(options, start=1):
        print(f"{i}. {option}")
    player = int(input("Your answer (enter the option number): "))
    if player == answer:
        print("Correct!")
        return True
    else:
        print(f"Sorry, that's incorrect. The correct answer was {answer}.")
        return False

def kbc_game():
    questions = [
        {
            "question": "The language of Lakshadweep. a Union Territory of India, is..",
            "options": ["Tamil", "Hindi", "Malayalam", "Telugu"],
            "answer": 3
        },
        {
            "question": "Which planet is known as the Red Planet?",
            "options": ["Mars", "Venus", "Jupiter", "Mercury"],
            "answer": 1
        },
                { 
            "question": "Bahubali festival is related to",
            "options": ["Islam", "Hinduism", "jainism", "Buddhism"],
            "answer": 4
        },
                {
            "question": "Which day is observed as the World Standards  Day?",
            "options": ["jun 26", "oct 14", "Nov 15", "Dec 2"],
            "answer": 3
        },
    ]

    score = 0
    for q in questions:
        if ask_question(q["question"], q["options"], q["answer"]):
            score += 1
        else:
            break  

    print(f"Your final score: {score}/{len(questions)}")

if __name__ == "__main__":
    print("Welcome to KBC - Who Wants to Be a Millionaire?")
    kbc_game()
