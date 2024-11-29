import random

def play_game():
    print("Welcome to the Number Guessing Game!")
    print("I have selected a number between 1 and 100. Can you guess it?")
    
    # Generate a random number
    number_to_guess = random.randint(1, 100)
    attempts = 0
    
    while True:
        try:
            # Get user input
            user_guess = int(input("Enter your guess: "))
            attempts += 1
            
            if user_guess < number_to_guess:
                print("Too low! Try again.")
            elif user_guess > number_to_guess:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You guessed the number in {attempts} attempts.")
                break
        except ValueError:
            print("Invalid input! Please enter a number.")

if __name__ == "__main__":
    play_game()

