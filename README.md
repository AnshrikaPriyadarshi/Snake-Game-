Project Title

Snake Game Using Python Turtle

Project Overview

This project is a simple interactive Snake Game developed in Python using the Turtle graphics library.

The player controls the snake using the W, A, S, and D keys. The snake moves continuously around the game window. When the snake reaches the food, the food moves to another position and the snake grows by one body segment.

The game also checks for:

Collision with the boundary of the game window

Collision with the snake's own body

When a collision occurs, the snake is reset to its starting position.

This project is designed to demonstrate basic Python programming concepts together with graphical interaction and modular programming.

Features

🎮 Keyboard-controlled snake movement

🍎 Food generation at different positions

🐍 Snake growth after eating food

🧱 Wall/boundary collision detection

🔄 Self-collision detection

♻️ Automatic snake reset after collision

🖥️ Simple graphical interface

📦 Modular Python file structure

Note: This version does not contain a score system, levels, lives, sound effects, or a database.

Technologies Used

Python 3

Turtle – for the graphical game window and game objects

Random – for generating new food positions

Time – for controlling the game delay

The project uses Python's standard libraries, so no external Python packages are required.

Requirements

To run the project, you need:

Python 3.x

A computer with a graphical desktop environment

A Python editor such as VS Code, IDLE, or PyCharm (optional)

Installation and Setup

Step 1: Download the project

Download or clone this GitHub repository.

Step 2: Open the project folder

Open the Snake-Game folder in your Python editor or terminal.

Step 3: Run the program

Run:

python main.py

The Snake Game window will open.

Controls

Key

Action

W

Move Up

S

Move Down

A

Move Left

D

Move Right

The snake cannot immediately move in the opposite direction. For example, while moving right, pressing A does not make the snake instantly reverse.

How the Game Works

The game follows this basic process:

Start Game
    ↓
Create Game Window
    ↓
Create Snake and Food
    ↓
Wait for Keyboard Input
    ↓
Change Snake Direction
    ↓
Move Snake
    ↓
Check Food Collision
    ↓
Food Collected?
   /  Yes  No
  ↓    ↓
Grow   Continue
Snake
  ↓
Check Wall / Body Collision
    ↓
Collision?
   /  Yes  No
  ↓    ↓
Reset  Continue Game
       ↓
    Repeat

Functional Requirements

1. Snake Control

The player can control the snake using the W/A/S/D keys.

2. Food and Growth

When the snake reaches the food:

The food is moved to a new position.

A new body segment is added to the snake.

3. Collision Handling

The program checks whether:

The snake reaches the game boundary.

The snake's head touches one of its own body segments.

If either condition occurs, the snake is reset.

Project Structure

Snake-Game/
│
├── main.py
├── snake.py
├── food.py
├── controls.py
├── collision.py
├── game.py
├── settings.py
├── README.md
├── statement.md
└── screenshots/

File Description

main.py

The main entry point of the project.

It:

Creates the Turtle window

Creates the snake

Creates the food

Sets up keyboard controls

Starts the game loop

snake.py

Contains the Snake class.

It handles:

Creating the snake head

Snake direction

Snake movement

Snake body segments

Snake growth

Resetting the snake

food.py

Contains the Food class.

It handles:

Creating the food

Moving the food to a new random position

Checking whether the snake has eaten the food

controls.py

Connects the keyboard keys to the snake's movement functions.

collision.py

Contains functions for:

Wall collision

Snake body collision

game.py

Contains the Game class and controls the main game loop.

It coordinates:

Screen updates

Collision checks

Food collection

Snake growth

Resetting after collisions

settings.py

Stores the main game settings, such as:

Window size

Colors

Snake movement distance

Game delay

Game boundary

System Architecture

                ┌───────────────┐
                │    Player     │
                └───────┬───────┘
                        │
                        ▼
                ┌───────────────┐
                │   controls.py │
                └───────┬───────┘
                        │
                        ▼
                ┌───────────────┐
                │    snake.py   │
                └───────┬───────┘
                        │
                        ▼
                ┌───────────────┐
                │    game.py    │
                └───┬───────┬───┘
                    │       │
          ┌─────────┘       └─────────┐
          ▼                           ▼
   ┌───────────────┐           ┌───────────────┐
   │    food.py    │           │ collision.py  │
   └───────────────┘           └───────────────┘
                    │
                    ▼
             ┌─────────────┐
             │ settings.py │
             └─────────────┘

Non-Functional Requirements

Usability

The controls are simple and use commonly understood W/A/S/D keys.

Performance

The game is lightweight and uses a small Turtle graphics window with a controlled update delay.

Reliability

The game continuously checks for food collection and collision conditions.

Maintainability

The program is divided into separate Python modules, making individual parts easier to understand and modify.

Resource Efficiency

The game does not require a database, server, internet connection, or external service.

Testing

The following tests can be performed to verify the game:

Test Case

Action

Expected Result

1

Run main.py

Game window opens

2

Press W

Snake moves upward

3

Press S

Snake moves downward

4

Press A

Snake moves left

5

Press D

Snake moves right

6

Move snake onto food

Snake grows and food changes position

7

Move snake into boundary

Snake resets

8

Move snake into its own body

Snake resets

9

Try immediate opposite direction

Opposite direction is ignored

Screenshots

Add screenshots of the running game to the screenshots/ folder.

Recommended screenshots:

Initial Game Screen – snake and food visible.

Snake Movement – snake moving in the game window.

Snake Growth – snake after eating food.

Collision/Reset – snake after reaching the boundary or its own body.

Example:

screenshots/
├── game_start.png
├── snake_movement.png
├── snake_growth.png
└── collision_reset.png

Challenges Faced

Some of the main implementation challenges were:

Making the snake move continuously.

Connecting keyboard input with the snake's direction.

Making the body segments follow the head.

Adding new body segments when food is collected.

Detecting collision with the game boundary.

Detecting collision between the snake's head and its body.

Resetting the snake correctly after a collision.

Organizing the program into separate modules.

Learning Outcomes

Through this project, the following concepts were practiced:

Python variables

Functions

Classes and objects

Lists

Loops

Conditional statements

Keyboard event handling

Random number generation

Collision detection

Game loops

Modular programming

Basic software testing

GitHub project organization

Future Enhancements

The current version can be extended in the future with:

Score system

Difficulty levels

Lives

Sound effects

Start and pause menus

High-score storage

Obstacles

Improved graphics

These features are not included in the current version.

Author

Anshrika Priyadarshi

Project Type

VITyarthi – Build Your Own Project

References

Python Documentation

Python Turtle Documentation

Python Random Documentation

Python Time Documentation

VITyarthi Build Your Own Project Guidelines
