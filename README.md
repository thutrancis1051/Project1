# Project1
Music Guessing Game

LINK TO YOUTUBE VIDEO https://youtu.be/XwATi8rjIrc

LINKS TO SONGS ON TUNEPAD
song 1) https://tunepad.com/project/57739
song 2) https://tunepad.com/project/57743
song 3) https://tunepad.com/project/57763
song 4) https://tunepad.com/project/57764
song 5) https://tunepad.com/project/57766

print("Hi there! Welcome to my CIS 1051 project.")
print("Head over to my link for Tunepad which is where I programmed the intros of 5 songs.")
print("One-by-one, you will choose your guess for each song here. Let's see how good of a musical ear you have!\n")

songs = [
    "What is song #1? (a) Hallelujah-Leonard Cohen (b) 18-1D (c) All Too Well-Taylor Swift",
    "What is song #2? (a) Beautiful Girls-Sean Kingston (b) Baby-Justin Bieber (c) Barbie Girl-Aqua",
    "What is song #3? (a) That's Amore-Dean Martin (b) Material Girl-Madonna (c) Mamma Mia-ABBA",
    "What is song #4? (a) Forever-Beach Boys (b) Let It Be-Beatles (c) Love in Vain-Rolling Stones",
    "What is song #5? (a) Another One Bites The Dust-Queen (b) Levitating-Dua Lipa (c) Roxanne-The Police"
]

answers = [
    ("c", "All Too Well-Taylor Swift"),
    ("b", "Baby-Justin Bieber"),
    ("c", "Mamma Mia-ABBA"),
    ("b", "Let It Be-The Beatles"),
    ("a", "Another One Bites The Dust-Queen")
    ]

def question_now(question, correct_answer):
    print(question)
    user_answer = input("Enter your answer (a,b, or c): ")
    if user_answer.lower() == correct_answer[0]:
        print("Correct! The answer is", correct_answer[1])
        return 1
    else:
        print("Incorrect, the answer is", correct_answer[1])
        return 0

score = 0
for i in range(len(songs)):
    score += question_now(songs[i], answers[i])

if score == 5:
    print("A perfect score! You have a good ear for music!")
elif score == 4:
    print("Great! You know your music pretty well!")
elif score == 3:
    print("Good job! You knew more than half of the songs!")
elif score == 2:
    print("")
else:
    print("Listen to more music.")
