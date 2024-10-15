
[Back to the README.md](README.md)


# Deck of Cards Drawing Program: Walkthrough Assignment

## Objective
You will create a Python program that simulates drawing a card from a deck. The program will use several functions that call one another to determine the card's suit and face value. You’ll also apply conditionals (if, elif, else) and return values to control the flow of your program. Follow each part carefully to ensure your program is complete and runs correctly.

## Part 1: Set Up Random Number Generation
Before starting the project, you will need to import Python’s random library to generate random numbers.

```python
import random
```

## Part 2: Function Breakdown

### 1. Create `roll_random(low, high)`
This function generates a random number between the given low and high values (inclusive). You will use this function throughout the program to roll numbers that decide the card's suit and face.

- **Parameters:** Two integers, `low` and `high`
- **Returns:** The randomly generated number

```python
def roll_random(low, high):
    . . .
```

### 2. Create `card_suit()`
This function determines the card's suit by rolling a random number between 1 and 100 using the `roll_random` function. It then assigns a suit based on the number rolled:
- "Hearts": If the roll is between 1 and 25
- "Clubs": If the roll is between 26 and 50
- "Diamonds": If the roll is between 51 and 75
- "Spades": If the roll is between 76 and 100

- **Returns:** A string with the card suit (e.g., "Hearts")

```python
def card_suit():
    ...
```

### 3. Create `card_face()`
This function determines the card's face value by rolling a random number between 1 and 10 using `roll_random`. It assigns the card's face as follows:
- "Ace": If the roll is 1
- 2-9: For rolls between 2 and 9, the face value is simply the rolled number converted to a string (e.g., "Two", "Three", etc.)
- 10: If the roll is 10, call the `royal()` function to assign a royal face value (i.e., Ten, Jack, Queen, or King)

- **Returns:** A string with the card face value (e.g., "Three")

```python
def card_face():
    . . .
```

### 4. Create `royal()`
This function rolls a number between 1 and 4 using `roll_random` to assign a royal face value:
- "Ten": If the roll is 1
- "Jack": If the roll is 2
- "Queen": If the roll is 3
- "King": If the roll is 4

- **Returns:** A string with the royal face value (e.g., "King")

```python
def royal():
    . . .
```

## Part 3: Drawing the Card

### 5. Create `draw_card()`
This function uses the previous functions to simulate drawing a card. It calls both `card_face()` and `card_suit()` to determine the card's face and suit, then prints a message stating which card was drawn.

- **Prints:** A readable statement like "You have drawn the Three of Hearts"

```python
def draw_card():
    . . .
```

## Part 4: Test Your Program
Now that all the functions are complete, you can test your program by calling `draw_card()` to simulate drawing a card from the deck.

```python
draw_card()
```

You can run the program multiple times to draw different cards each time, thanks to the random number generation.

## Part 5: Optional Enhancements (if you’re bored)
- **Multiple Draws:** Modify the program to draw a specified number of cards in a row.
- **Card Collection:** Store drawn cards in a list and display them all at the end.
- **Exclude Drawn Cards:** Modify the program so that drawn cards are removed from the deck and cannot be drawn again.
- **Jokers:** Add a small chance (e.g., 2%) that the player draws a Joker card.

## Deliverables
- **Source Code:** Submit all Python files for your game. This should be through a Codespace share link.
- **Game Demo:** Prepare a short demonstration of your game (run through a few rooms, show combat, and inventory management). The demo should be a screen recording less than 1 minute in length.
- **Optional Enhancements (if completed):** Demonstrate the additional features added for extra credit.

## Grading Criteria
- **Functionality:** Does the program simulate drawing a card as described?
- **Code Structure:** Are functions correctly used and are return values handled properly?
- **Code Quality:** Is the code well-organized, commented, and easy to read?
- **Creativity:** Did you add any optional enhancements or go beyond the basic requirements?