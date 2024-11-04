# Team-work- by Takhmina & Fahad
#10/29/24

# first import random module
# then input random numbers from 1 to 10 
# user needs to enter a number between 1 - 10
# if user's guessed number is less than 1 or greater than 10 then it will not work 
# and it will prompt as " Please guess a number between 1 - 10"
# if user guessed lower num then it will ask to enter higher num
# Nest input: Please guess higher number
# if user didn't get guessed higher num it will prompt as "You guessed a wrong number"
# if user guessed correct number then it will prompt congrats  
# All set
# Program will finish
# if user guessed higher num then it will ask to enter lower num
# Nest input: Please guess lower number
# if user didn't get guessed lower num it will prompt as "You guessed a wrong number"
# if user guessed correct number then it will prompt congrats  
# All set
# Program will finish
# Below is our coding and we have also uploaded our python file of our coding. 

# By Shaik Fahad & Takhmina Ulukmanova
# Nov 02, 2024

# The program, which we created, will generate a guess-number game.

import random
# Step 1: In order to create a guess number we have to import random module.
random_number = random.randint(1,10)

user_guess = None

while user_guess != random_number:
    # step 2: creating a loop.
    user_guess = int(input("Please guess number between 1 and 10: "))
        # step 3: input from user.

    if user_guess < 1 or user_guess > 10:
        print("You have to guess a number between 1 and 10.")
        # step 4: if user guess num is less than 1 or greater than 10 then it will not work.
    elif user_guess < random_number:
        print("Higher! Try again.")
            # step 5: if user num is higher then it will prompt higher num, so user has to guess lower num.
        higher_guess = int(input("Please guess a higher number: "))
        
        if higher_guess < 1 or higher_guess > 10:
            print("You have to guess a number between 1 and 10.")
                #step 6: if user guess num is less than 1 or greater than 10 then it will not work.
        elif higher_guess == random_number:
            print(f"Well done, you guessed correct: {random_number}")
                # step 7: if user guessed correct num then it will finish program.
        else:
            print("That's still not correct. Try again!")
                # step 8: if still incorrect it will ask for lower or higher num or it will finish the program.
    elif user_guess > random_number:
        print("Lower! Try again.")
        higher_guess = int(input("Please guess a lower number: "))
                # step 9:  Provide a hint to guess lower Prompt the user to guess a lower number
        
        if higher_guess < 1 or higher_guess > 10:
            print("You have to guess a number between 1 and 10.")
                # step 10: if user guess num is less than 1 or greater than 10 then it will not work.
        elif higher_guess == random_number:
            print(f"Well done, you guessed correct: {random_number}")
                # steo 11: if user guessed correct num then it will finish program.
        else:
            print("That's still not correct. Try again!")
            # step 12: if still incorrect it will ask for lower or higher num or it will finish the program
    else:
        print(f"Well done, you guessed correct: {random_number}")
