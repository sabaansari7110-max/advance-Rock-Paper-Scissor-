# Advance-Rock-Paper-Scissor- Terminal Edition

A simple, fun Rock-Paper-Scissors game you play against the computer right in your terminal.

First to **5 wins** takes the match!

## Features

- Classic rules: Rock beats Scissors, Scissors beats Paper, Paper beats Rock
- Best of unlimited rounds → first to 5 wins
- Simple text-based interface
- Computer opponent with random choices
- Score tracking
- Clear round-by-round feedback
- Play again option

## How to Play

```bash
# Clone the repository (if you haven't already)
https://github.com/sabaansari7110-max/advance-Rock-Paper-Scissor-.git
cd rock-paper-scissors-terminal
```
copy code
```python
# Rock-Paper-Scissor-game
# A simple Rock, paper, Scissor game built using python. The user plays against the computer in the terminal, and the winner is decided based on classic game rules.


import random

def get_player_choice():
    while True:
        print("\nChoose: (r)ock  (p)aper  (s)cissors  (q)uit")
        choice = input("> ").lower().strip()
        
        if choice in ['r', 'rock']:
            return 'rock'
        elif choice in ['p', 'paper']:
            return 'paper'
        elif choice in ['s', 'scissors']:
            return 'scissors'
        elif choice in ['q', 'quit']:
            print("Thanks for playing! 👋")
            exit()
        else:
            print("Invalid choice. Please try again.")

def get_computer_choice():
    return random.choice(['rock', 'paper', 'scissors'])

def determine_winner(player, computer):
    if player == computer:
        return "tie"
    elif (player == 'rock' and computer == 'scissors') or \
         (player == 'scissors' and computer == 'paper') or \
         (player == 'paper' and computer == 'rock'):
        return "player"
    else:
        return "computer"

def print_result(player, computer, winner, player_score, computer_score):
    print(f"\nYou chose:     {player.upper()}")
    print(f"Computer chose: {computer.upper()}")
    
    if winner == "tie":
        print("→ It's a tie!")
    elif winner == "player":
        print("→ You win this round! 🎉")
    else:
        print("→ Computer wins this round! 💻")
    
    print(f"Score →  You: {player_score}  |  Computer: {computer_score}\n")

def main():
    print("=====================================")
    print("     ROCK PAPER SCISSORS - Terminal")
    print("       First to 5 wins the game!")
    print("=====================================\n")
    
    player_score = 0
    computer_score = 0
    win_goal = 5
    
    while True:
        player_choice = get_player_choice()
        computer_choice = get_computer_choice()
        
        winner = determine_winner(player_choice, computer_choice)
        
        if winner == "player":
            player_score += 1
        elif winner == "computer":
            computer_score += 1
        
        print_result(player_choice, computer_choice, winner, player_score, computer_score)
        
        # Check for game end
        if player_score >= win_goal:
            print("╔════════════════════════════╗")
            print("║     YOU WIN THE GAME! 🎊     ║")
            print("╚════════════════════════════╝")
            break
        elif computer_score >= win_goal:
            print("╔════════════════════════════╗")
            print("║   COMPUTER WINS THE GAME!  ║")
            print("╚════════════════════════════╝")
            break
    
    # Play again?
    while True:
        again = input("\nPlay again? (y/n): ").lower().strip()
        if again in ['y', 'yes']:
            print("\n" + "-"*40 + "\n")
            main()          # Restart the game
            return
        elif again in ['n', 'no']:
            print("Goodbye! Thanks for playing.\n")
            return
        else:
            print("Please answer y or n.")

if __name__ == "__main__":
    main()
y
```
Make sure python is installed.

# Run the game (choose the command depending on your implementation)
python3 rps.py
## or
python rps.py

## Just type:
<br>
r or rock
<br>
p or paper
<br>
s or scissors
<br>
Type q or quit to exit the game at any time.
<br> 

# Example Gameplay
## Rock Paper Scissors - First to 5 Wins
-------------------------------------
Round 1
Your choice (r/p/s): rock

You: Rock
Computer: Scissors
→ You win this round!

Score: You 1 – Computer 0

Round 2
Your choice (r/p/s): p

You: Paper
Computer: Scissors
→ Computer wins!

Score: You 1 – Computer 1
<br>
=====================================
<br>
          GAME FINISHED!
          <br>
=====================================
Final Score: You 5 – Computer 3
YOU WIN THE MATCH! 🎉

Play again? (y/n):
# Requirements
Python 3.x (if Python version)
No external libraries needed.

## Possible Future Improvements (feel free to add)
-Add difficulty levels (dumb / normal / evil computer)
<br>
-Keep match history / win streak
<br>
-Add funny taunts from the computer
<br>
-ASCII art for hands
<br>
-Score saving between sessions.
<br>
-Have fun and may your throws always be strong! ✊✌️✋
<br>


```markdown
# RPS Terminal
```
Super simple Rock-Paper-Scissors in your terminal.  
First to **5 wins**.
```
```bash
python3 rps.py
# or python rps.py
Just type: rock / paper / scissors (or r/p/s)
Enjoy!
```
