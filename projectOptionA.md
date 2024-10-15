[Back to the README.md](README.md)


# Text-Based Adventure Game: Walkthrough Assignment

## Objective
You will create a text-based adventure game where the player explores a virtual world, encounters enemies, collects items, and works toward a final goal (e.g., defeating a boss or escaping a dungeon).

This guide will help you build the game step by step. Follow each section carefully and make sure to include all required features. Do not copy the examples, make your own and add to the examples to get full marks on your project grade.

## Part 1: Game Structure

### 1. Introduction and Setup
Create a function that will introduce the game to the player and explain the game’s goal.

Example:
```python
def introduction():
    print("Welcome to the Dungeon Escape!")
    print("Your goal is to explore the dungeon, collect items, and defeat the final boss.")
    print("Good luck!")
```

### 2. Player Attributes
You need to track the player’s health and inventory. These will be stored in variables. Create a function to show the player's current status, named `show_status`.

### 3. Room Navigation
Create a function to navigate between different rooms. Each room should have a description, and the player should be able to move by typing directions like "go north" or "enter cave." Start with at least 5 rooms. Each function will be named, `room1`, `room2`, `room3`, etc.

Example:
```python
def room1():
    print("You are in a dark room with a door to the north.")
    action = input("What do you want to do? (type 'go north' or 'explore') ").lower()
    if action == 'go north':
        room2()
    elif action == 'explore':
        print("You found a health potion!")
        inventory.append('health potion')
        room1()

def room2():
    print("You have entered a room with a strange smell. There's a door to the east.")
    action = input("What do you want to do? (type 'go east' or 'explore') ").lower()
    if action == 'go east':
        room3()
    else:
        room2()
```

Repeat this structure for more rooms.

### 4. Enemy Encounters
In some rooms, the player may encounter an enemy. Create a simple combat system where the player can choose to fight or flee. Create an enemy encounter function named `enemy_encounter`.

Example:
```python
def room7():
    print("You are in a damp cave. There's a goblin here!")
    enemy_encounter()
    room2()
```

### 5. Inventory Management
Players can collect items, such as health potions. Create a function that allows them to use these items. These items can add to the health, or power, etc. They could take away from aura, or intelligence if they are in too high of a dose… Be creative!

### 6. Health System
If the player’s health drops to 0, they lose the game. You can create a function to check if the player is alive:

Example:
```python
def check_health():
    ...
```

Call this function regularly during the game to ensure the player’s health is tracked, and end the game if it reaches zero.

## Part 2: Game Mechanics

### 1. Winning and Losing Conditions
The player wins by achieving a specific goal, such as defeating a final boss or escaping the dungeon. Add a function to end the game when they win:

Example:
```python
def final_room():
    print("You have entered the final chamber. A dragon awaits!")
    enemy_encounter()  # You can reuse the enemy_encounter function for the final boss.
    
    if player_health > 0:
        print("Congratulations! You have defeated the dragon and escaped the dungeon.")
```

## Part 3: Putting It All Together
Create a main game loop that ties all the functions together. The player should be able to move between rooms, encounter enemies, and use items.

Example:
```python
def start_game():
    introduction()
    room1()  # Start in the first room

start_game()
```

You should call the `check_health()` function after combat or other actions to ensure the player is alive, and the game can end if they lose.

## Part 4: Optional Enhancements (if you’re bored)
- **Multiple Enemy Types**: Create different types of enemies with varying health and attack strength.
- **More Items**: Add items with different effects, like increasing attack power.
- **More Complex Combat**: Introduce more strategy to combat, such as allowing players to choose between different types of attacks.
- **Puzzle Elements**: Add simple puzzles the player has to solve to progress, such as finding a key to unlock a door.

## Deliverables
- **Source Code**: Submit all Python files for your game. This should be through a Codespace share link.
- **Game Demo**: Prepare a short demonstration of your game (run through a few rooms, show combat, and inventory management). The demo should be a screen recording less than 1 minute in length.

## Grading Criteria
- **Functionality**: Does the game run as expected? Are all core features implemented (room navigation, combat, inventory)?
- **Code Quality**: Is the code organized, commented, and easy to follow?
- **Creativity**: How creative and engaging is the game’s narrative and design?
- **Completion**: Did you include all required features from the walkthrough?