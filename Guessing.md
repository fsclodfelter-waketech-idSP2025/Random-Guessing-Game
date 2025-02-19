# Random Number Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Let's Begin!]) --> GenerateRandomNumber{Generate a Secret Number}
    GenerateRandomNumber --> InputGuess[What's Your Guess?]
    InputGuess --> ValidateInput{Is the Guess Valid?}
    ValidateInput -->|No| InvalidInput[_Whops!_ Please enter a valid number.]
    InvalidInput --> InputGuess
    ValidateInput -->|Yes| CompareGuess{Comparing Numbers}
    CompareGuess -->|No, Too High| TooHigh[_Oops!_ **Too High!** Try a another number.]
    CompareGuess -->|No, Too Low| TooLow[_Ooo No!_ **Too Low!** Try another number.]
    CompareGuess -->|Yes| Correct[_**Congratulations!**_ You guessed it!]
    TooHigh --> InputGuess
    TooLow --> InputGuess
    Correct --> End([_**Correct!**_ Well Done! Game Over!])
