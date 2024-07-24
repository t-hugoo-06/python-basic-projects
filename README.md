# Here's the code for a simple Mad Libs game I wrote in about 30 min using python. Feel free to add adjustments and send them to me; I just started coding and I want to improve.
# GAME LOGIC:
# So for those who don't know, Mad Libs is basically a game where a player enters random words of their choice which are then put into a random sentence (which the player doesn't see until before saying the words)
  # I created a 'get_user_input()' function to ensure that I get valid input from the user, that means no empty strings and only alphabetical letters
  # I created a 'mad_libs()' function that is basically the main function. 

# CODE


import random 

def get_user_input(prompt):
    while True:
        user_input = input(prompt)
        if user_input.isalpha():
            return user_input
        print('Please enter a value.')

def mad_libs():
    play = input("Welcome to Mad Libs! A hilarious game to play with friends or family no matter the occasion. \nDo you want to play? (yes or no) ")
    while play.lower() == 'yes':
        print("Yay, let's start!")
        print("Please enter a word for each category.")

        noun = get_user_input("Enter a noun: ")
        adj = get_user_input("Enter an adjective: ")
        adv = get_user_input("Enter an adverb: ")
        verb = get_user_input("Enter a verb: ")

        ml_list = [
            f"Hello {noun}, how you doin'? You look {adj} today, no wonder those people kept looking {adv} at you. Anyway, I hope you remembered to {verb} the cat.",
            f"Once upon a time, there was a {adj} {noun} who loved to {verb} {adv}. Everyone in the village admired the {noun} for its unique talent.",
            f"In a faraway land, a {adj} {noun} decided to {verb} {adv} through the enchanted forest. The {noun} encountered many magical creatures along the way.",
            f"The {adj} {noun} {adv} {verb} across the galaxy. Its mission was to find a new home for its people, but the journey was filled with unexpected challenges.",
            f"On a dark and stormy night, the {adj} {noun} {adv} {verb} into the abandoned mansion. Little did it know, the mansion held secrets that would change its life forever.",
            f"One day, a {adj} {noun} decided to {verb} {adv} in the middle of the town square. The {noun} caused quite a commotion, leaving everyone in stitches of laughter."
        ]

        print(random.choice(ml_list))

        play = get_user_input("Do you want to keep playing? ")
    print('Thanks for playing!')

mad_libs()
