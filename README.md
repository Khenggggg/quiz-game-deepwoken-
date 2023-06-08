# quiz-game-deepwoken-
hmmmmm

questions = ("How many elements are in deepwoken?: ",
                       "Which bosses give the most legendary weapon?: ",
                       "What is the most abuses of hybird talent that make game cracking?: ",
                       "How many weapon type in deepwoken?: ",
                       "Which how much world type in deepwoken?: ")

options = (("A. 1", "B. 5", "C. 3", "D. 4"),
                   ("A. Erthions", "B. Ferryman", "C. Duke", "D. Primadon"),
                   ("A. 10", "B. 4", "C. 7", "D. 5"),
                   ("A. 3(overworld, the depth, layer 2)", "B. 2(overworld, s", "C. Earth", "D. Mars"))

answers = ("C", "D", "A", "A", "B")
guesses = []
score = 0
question_num = 0

for question in questions:
    print("----------------------")
    print(question)
    for option in options[question_num]:
        print(option)

    guess = input("Enter (A, B, C, D): ").upper()
    guesses.append(guess)
    if guess == answers[question_num]:
        score += 1
        print("CORRECT!")
    else:
        print("INCORRECT!")
        print(f"{answers[question_num]} is the correct answer")
    question_num += 1

print("----------------------")
print("       RESULTS        ")
print("----------------------")

print("answers: ", end="")
for answer in answers:
    print(answer, end=" ")
print()

print("guesses: ", end="")
for guess in guesses:
    print(guess, end=" ")
print()

score = int(score / len(questions) * 100)
print(f"Your score is: {score}%")
