# This my random number game.
# This was my first ever project, and the project I used to learn python coding.
import random
import time
from os import system, name
def clear():
	if name == 'nt':
		_ = system('cls')
	else:
		_ = system('clear')
def dictionary():
    print('dictionary() : What you are seeing right now')
    print('clear() : Clears the console.')
    print('game() : The command to run the game.')
    print('quit() : Ends the Repl process.')
    print('rules() : Explains the rules of the game.')
def rules():
    print('You, the player, have to try and guess the number, I, the computer, came up with. This number is completely random. You can change a few rules of the game yourself. One: You can change how many guesses you get to guess my number. Two: You can change the number range that I can choose from. 1 through 10, 1 through 20, etc. If you guess my number correctly, you win.')
def game():
    y = 8
    x = 0.5
    x = float(x)
    z = input("Would you like to play the number guessing game?(1 = Yes , 2 = No)\n")
    z = int(z)
    if z == 2:
        quit()
    if z == 1:
        print('Okay, so, the rules of the game are you have to try and guess my number within a certain amount of guesses.')
        print("You can choose how many guesses you get (as long as it isn't zero) and the number limit (as long as it isn't 1 or 0) I can choose from. 1 through 10, 1 through 20, etc.")
        time.sleep(y)
        print("Got it?")
        time.sleep(x)
        print("Good.")
    time.sleep(5)
    a = input('How many guesses woukd you like?\n')
    a = int(a)
    if a == 0:
        a = input("Sorry, that doesn't work. Pick a different number\n")
    else:
        a = str(a)
        b = input("Ok then, if you want " + a + " guesses, what is the number limit. 1 through \n")
    b = int(b)
    if b == 1:
        print("Sorry, that doesn't work. Stop the program and run again.")
    if b == 0:
        print("Sorry, that doesn't work. Stop the program and run again.")
    guessesTaken = 0
    number = random.randint(1,b)
    if b > 1:
        b = str(b)
        print("Pick a number between 1 and " + b + "." + " If you're right, you win.")
    b = int(b)
    a = int(a)
    while guessesTaken < a:
        guess = input()
        guess = int(guess)
        guessesTaken = guessesTaken + 1
        if guess < number:
            print("Wrong, try again.")
        if guess > number:
            print("Wrong, try again.")
        if guess == number:
            break
    if guess == number:
        guessesTaken = str(guessesTaken)
        print("Good Job, that was my number! You guessed it in " + guessesTaken + " guesses.")
    if guess != number:
        number = str(number)
        print("That is wrong. My number was " + number)
    print("Thanks for using the Program. Feel free to fork it for whatever you are using.\nDon't forget to like and leave a comment. Please and Thankyou.\nDon't forget to type dictionary() if you want to see all the commands for the game.")
game()
