









import random
import math

def game():
    # Taking Inputs
    player = input("Enter your name : ")

    lower = int(input("Enter Lower bound: "))
    # Taking Inputs
    upper = int(input("Enter Upper bound: "))

    if(lower<upper):
        # generating random number between
        # the lower and upper
        x = random.randint(lower, upper) #randint means random integer from lower bound given to upper bound 
        print(f"\n\t{player} You've only ", math.ceil(math.log(upper - lower + 1, 2)), " chances to guess the number!\n")

        #math.log means log(value,base)

        # Initializing the number of guesses.
        count = 0

        # for calculation of minimum number of
        # guesses depends upon range

        while count < math.log(upper - lower + 1, 2):
            count += 1

            # taking guessing number as input
            print(f"Guess a number between {lower} and {upper} : ")
            guess = int(input())

            # Condition testing
            if x == guess:
                print(f"Congratulations {player} you did it in {count} try")
                # Once guessed, loop will break
                break

            elif x > guess:
                print("You guessed small!")
            elif x < guess:
                print("You Guessed high!")

        # If Guessing is more than required guesses,
        # shows this output.

        if count >= math.log(upper - lower + 1, 2):
            print("\nThe number is %d" % x)
            print("\tBetter Luck Next time"+player+"!")
        
    else:
        print(f"\n{player} please Check Upper Bound and Lower Bound Values\n")


game()
print("\nPress 1 to play and 2 to exit...\n")
x = int(input())
while(x):
    game()
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
