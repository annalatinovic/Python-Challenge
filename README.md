# Python-Challenge
import random

user_name = input("What is your name?")

print("Welcome " + user_name + " to the Guessing Game.")

min = int(input("Please enter a minimum value for the range: "))

max = int(input("Please enter a maximum value for the range: "))

if min > max:
	print("The maximum value needs to be greater than the minimum value.")
	max = int(input("Please enter a maximum value: "))

computer_generator = (random.randint(min,max))

user_input = input("Please guess a number that is in the range of " + str(min) + " and " + str(max) + ": ")

if user_input.isdigit():
    user_input = int(user_input)
    while user_input is not computer_generator:
        if user_input > computer_generator:
            print("Incorrect. The number is lower.")
            user_input = int(input("Please guess a number that is in the range of " + str(min) + " and " + str(max) + ": "))
        elif user_input < computer_generator:
            print("Incorrect. The number is higher.")
            user_input = int(input("Please guess a number that is in the range of " + str(min) + " and " + str(max) + ": "))
    else:
        print("Congratulations! You guessed the number.")
else:
    print("Error. Only integers are allowed.")
    user_input = input("Please guess a number that is in the range of " + str(min) + " and " + str(max) + ": ")
    while user_input is not computer_generator:
        user_input = int(user_input)
        if user_input > computer_generator:
            print("Incorrect. The number is lower.")
            user_input = int(input("Please guess a number that is in the range of " + str(min) + " and " + str(max) + ": "))
        elif user_input < computer_generator:
            print("Incorrect. The number is higher.")
            user_input = int(input("Please guess a number that is in the range of " + str(min) + " and " + str(max) + ": "))
    else:
        print("Congratulations! You guessed the number.")
