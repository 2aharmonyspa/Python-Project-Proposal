# Python-Project-Proposal
#I'm going to improve the dictionary portion
import random

class Question:
    def __init__(self, text, is_true):
        self.text = text
        self.is_true = is_true

class Object:
    def __init__(self, name, questions):
        self.name = name
        self.questions = questions

def play_game(objects):
    print("Welcome to Guess the Object! Think of an object and answer the following questions:")
    while True:
        obj = random.choice(objects)
        for question in obj.questions:
            answer = input(question.text + " (y/n) ")
            if answer.lower() == "y" and not question.is_true:
                break
            elif answer.lower() == "n" and question.is_true:
                break
        else:
            print("I think your object is " + obj.name + "!")
            play_again = input("Do you want to play again? (y/n) ")
            if play_again.lower() == "n":



            
                return

if __name__ == "__main__":
     #Object("Couch", [Question("Can you sit on your object?", True),
                         #Question("Is it a couch or chair?", True)]),
    a = input('can you sit')
    b = input('is it a couch')
    diction = {'TrueTrue':'couch'}
    print(diction[a+b])
    pillow = 1
    {"soft":['pillow','chair','couch']}
    #play_game(objects)
