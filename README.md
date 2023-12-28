# Rock, Paper, Scissors Game in Python

## Introduction
This Python program allows users to play the classic Rock, Paper, Scissors game against the computer.

## How to Play
1. Run the script in a Python environment.
2. Enter your choice: "rock," "paper," or "scissors."
3. The computer will randomly select its move.
4. The winner will be determined based on the game rules:
   - Rock crushes scissors
   - Scissors cuts paper
   - Paper covers rock

## Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/Shubham-Zone/RPS-python.git   ```

2. Navigate to the project directory:
   ```bash
   cd RPS-Python
   ```

3. Run the script:
   ```bash
   python rps_game.py
   ```

## Code Explanation

```python
import random

def get_user_choice():
    """Get user's choice."""
    user_choice = input("Enter 'rock', 'paper', or 'scissors': ").lower()
    return user_choice

def get_computer_choice():
    """Generate a random choice for the computer."""
    choices = ['rock', 'paper', 'scissors']
    computer_choice = random.choice(choices)
    return computer_choice

def determine_winner(user_choice, computer_choice):
    """Determine the winner of the game."""
    if user_choice == computer_choice:
        return "It's a tie!"
    elif (
        (user_choice == 'rock' and computer_choice == 'scissors') or
        (user_choice == 'scissors' and computer_choice == 'paper') or
        (user_choice == 'paper' and computer_choice == 'rock')
    ):
        return "You win!"
    else:
        return "Computer wins!"

def play_game():
    """Main function to play the game."""
    user_choice = get_user_choice()
    computer_choice = get_computer_choice()
    
    print(f"You chose: {user_choice}")
    print(f"Computer chose: {computer_choice}")

    result = determine_winner(user_choice, computer_choice)
    print(result)

# Run the game
if __name__ == "__main__":
    play_game()
```

The code defines functions for getting user and computer choices, determining the winner, and the main function to play the game. The choices are compared, and the winner is declared based on the game rules.
