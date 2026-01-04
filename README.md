Pac-Man AI Game (Python + Pygame)
Overview

This project is a fully autonomous Pac-Man game implemented in Python using Pygame. Unlike traditional Pac-Man implementations that rely on player input, Pac-Man in this game is controlled entirely by artificial intelligence.

The AI continuously evaluates the maze, ghost positions, and game state to make real-time decisions using A* pathfinding combined with safety heuristics. The project demonstrates applied algorithms, real-time decision making, and clean modular game architecture.

Features
Core Gameplay

Classic Pac-Man mechanics implemented from scratch

Pellet and power-pellet consumption

Score tracking and level progression

Game over and win states with end screens

Artificial Intelligence

A* pathfinding for Pac-Man navigation

Dynamic target selection based on:

Ghost proximity

Power mode status

Pellet value and safety

Continuous path re-evaluation when threats change

Warp tunnel awareness built directly into the heuristic

Ghost Behavior

Four independent ghosts with distinct states

Chase and flee behaviors depending on power mode

Respawn logic after being eaten

Warp tunnel traversal with cooldowns and slowdowns

Randomized movement elements to reduce predictability

Level System

Multiple handcrafted maze layouts

Increasing difficulty through layout complexity

Automatic reset and progression between levels

Technical Highlights
Pathfinding and Decision Logic

Manhattan-distance-based A* heuristic

Ghost proximity penalties dynamically injected into path cost

Safety checks on both candidate targets and intermediate paths

Separate logic for escape behavior, power pellet pursuit, and pellet collection

Rendering

Grid-based maze rendering

Animated Pac-Man mouth

Color-coded ghosts with state-based color changes

Heads-up display showing score and current level

Performance

Fixed timestep game loop

Lightweight data structures

No external AI or pathfinding libraries used

Project Structure

pacman/

constants.py

Screen dimensions, colors, and timing constants

Maze layouts and level data

rendering.py

Maze drawing

Pac-Man animation

Ghost rendering

HUD and end screens

game_logic.py

A* pathfinding implementation

Ghost AI and movement logic

Collision detection

Target selection heuristics

Level reset utilities

init.py

Package marker

main.py

Game loop and state management

AI coordination

Rendering orchestration

requirements.txt
README.md
.gitignore

Installation
Prerequisites

Python 3.9 or newer

pip package manager

Setup

Clone the repository:

git clone https://github.com/yourusername/pacman_game.git

cd pacman_game

Install dependencies:

pip install pygame

Run the game:

python main.py

Controls

This game has no player controls.

Pac-Man is fully AI-controlled and navigates the maze autonomously using A* pathfinding and dynamic decision logic.

Gameplay Mechanics
Power Mode

Activated when Pac-Man consumes a power pellet

Ghosts become vulnerable and can be eaten

Pac-Man actively targets nearby ghosts

Ghosts respawn after a short delay

Warp Tunnels

Located on the central row of the maze

Allow instant horizontal teleportation

Integrated into both Pac-Man and ghost movement logic

Ghosts experience a delay after warping for balance

Educational Value

This project demonstrates:

A* pathfinding in a dynamic adversarial environment

Heuristic design beyond shortest-path problems

State-based AI behavior

Real-time simulation and game loops

Clean, modular Python architecture

It is well suited for:

Algorithms coursework

Artificial intelligence demonstrations

Game development portfolios

Software engineering examples

License

MIT License

You are free to use, modify, and distribute this project with attribution.
