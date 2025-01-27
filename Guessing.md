# Guessing Game

```mermaid
flowchart TD
    A([Start]) ---> B{Generate random number from 1-100}
    B --> C[User inputs their guess]
    C --> D{Is the input a valid input?}
    D -->|No| E((Invalid input. Enter a number within the range 1-100))
    E ----> |Repeat| C
    D -->|Yes| F{Is the guess correct?}
    F -->|Yes| G[Congrats you got it right!]
    F -->|No| H((Is the guess too high?))
    H -->|Yes| I[The guess was too high]
    H -->|No| J[The guess was too low]
    I --> K[Try Again]
    J --> K[Try Again]
    K ----> |Repeat| C
    G ----> L([End])

```
# Description
1. Step A: Starts the Game
2. Step B: The computer generates a random number between 1 to 100
3. Step C: Gets the user input
4. Step D: Checks if the user's input is valid
5. Step E: Determines the user's input is invalid and reiterates to the user to choose a number between 1 and 100. Goes back to Step C
6. Step F: Checks if the user's guess is correct.
7. Step G: The user's guess is correct. Goes to Step L
8. Step H: Checks if the user's guess was too high.
9. Step I: Determines the user's guess was too high. Goes to Step K
10. Step J: Determines the user's guess was too low. Goes to Step K
11. Step K: Lets the user guess again. Goes back to Step C
12. Step L: Ends the Game
