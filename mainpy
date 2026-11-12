import random

print("Welcome to Rock, Paper, Scissors!")
choices = ["rock", "paper", "scissors"]

# While loop to keep the overall program running for multiple matches
playing_game = True
while playing_game:
    print("\n--- New Match Started ---")
    user_score = 0
    computer_score = 0
    
    # For loop to play a fixed number of rounds per match (e.g., 3 rounds)
    for round_num in range(1, 4):
        print(f"\nRound {round_num} of 3")
        user_choice = input("Enter rock, paper, or scissors (or type 'quit'): ").lower()
        
        if user_choice == 'quit':
            playing_game = False
            break
            
        if user_choice not in choices:
            print("Invalid choice. You lose this round's turn!")
            continue
            
        computer_choice = random.choice(choices)
        print(f"Computer chose: {computer_choice}")
        
        # Determine the winner of the round
        if user_choice == computer_choice:
            print("It's a tie!")
        elif (
            (user_choice == "rock" and computer_choice == "scissors") or
            (user_choice == "paper" and computer_choice == "rock") or
            (user_choice == "scissors" and computer_choice == "paper")
        ):
            print("You win this round!")
            user_score += 1
        else:
            print("Computer wins this round!")
            computer_score += 1
            
    # If the user typed 'quit' inside the for loop, break out of the while loop too
    if not playing_game:
        break
        
    # Match Summary
    print("\n--- Match Over ---")
    print(f"Final Score -> You: {user_score} | Computer: {computer_score}")
    if user_score > computer_score:
        print("🎉 Congratulations, you won the match!")
    elif computer_score > user_score:
        print("💻 Computer won the match! Better luck next time.")
    else:
        print("🤝 It's a tie match!")
        
    # Ask if the user wants to play another match
    play_again = input("\nDo you want to play another match? (yes/no): ").lower()
    if play_again != 'yes':
        playing_game = False

print("\nThanks for playing!")
