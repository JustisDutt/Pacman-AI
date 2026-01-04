# Pac-Man AI Game (Python + Pygame)

## Overview

This project is a fully autonomous implementation of the classic Pac-Man game, built in Python using Pygame. Unlike traditional Pac-Man versions that rely on player input, Pac-Man in this project is controlled entirely by artificial intelligence.

The AI uses A* pathfinding combined with real-time heuristics to navigate the maze, avoid ghosts, pursue power pellets, and strategically hunt ghosts during power mode. The project emphasizes algorithmic decision making, clean architecture, and readable, maintainable code, reflecting the standards expected of a graduating computer science student.

---

## Features

### Gameplay
- Classic Pac-Man mechanics implemented from scratch
- Pellet and power-pellet consumption
- Score tracking and multi-level progression
- Game over and win screens

### Artificial Intelligence
- A* pathfinding for autonomous Pac-Man navigation
- Dynamic target selection based on:
  - Ghost proximity
  - Power mode state
  - Pellet value and safety
- Continuous path re-evaluation when the environment changes
- Warp tunnel awareness integrated into pathfinding heuristics

### Ghost AI
- Four independent ghosts with individual states
- Context-aware chase and flee behavior
- Respawn system after being eaten
- Warp tunnel traversal with delays and slowdowns
- Randomized movement elements to prevent deterministic behavior

---

## Technical Highlights

### Pathfinding and Decision Logic
- Manhattan-distance-based A* heuristic
- Dynamic ghost proximity penalties added to path costs
- Safety checks applied to both targets and intermediate paths
- Separate logic for:
  - Escape behavior
  - Power pellet pursuit
  - Pellet optimization

### Rendering
- Grid-based maze rendering
- Animated Pac-Man mouth
- Color-coded ghosts with state-based color changes
- Heads-up display showing score and current level

### Performance
- Fixed timestep game loop
- Lightweight data structures
- No external AI or pathfinding libraries

---

## Project Structure

```text
pacman/
├── constants.py
│   ├── Screen dimensions, colors, and timing constants
│   └── Maze layouts and level data
├── rendering.py
│   ├── Maze drawing
│   ├── Pac-Man animation
│   ├── Ghost rendering
│   └── HUD and end screens
├── game_logic.py
│   ├── A* pathfinding implementation
│   ├── Ghost AI and movement logic
│   ├── Collision detection
│   ├── Target selection heuristics
│   └── Level reset utilities
└── __init__.py

main.py
├── Game loop and state management
├── AI coordination
└── Rendering orchestration

requirements.txt
README.md
.gitignore
```

---

## Installation

### Prerequisites
- Python 3.9 or newer
- pip package manager

### Setup

Clone the repository:
```bash
git clone https://github.com/yourusername/pacman_game.git
cd pacman_game
```

Install dependencies:
```bash
pip install pygame
```

Run the game:
```bash
python main.py
```

---

## Controls

This game has no player controls.

Pac-Man is fully AI-controlled and navigates the maze autonomously using A* pathfinding and dynamic decision logic.

---

## Gameplay Mechanics

### Power Mode
- Activated when Pac-Man consumes a power pellet
- Ghosts become vulnerable and can be eaten
- Pac-Man actively targets nearby ghosts
- Ghosts respawn after a short delay

### Warp Tunnels
- Located on the central row of the maze
- Allow instant horizontal teleportation
- Integrated into both Pac-Man and ghost movement logic
- Ghosts experience a delay after warping for balance

---

## Educational Value

This project demonstrates:
- A* pathfinding in a dynamic adversarial environment
- Heuristic design beyond shortest-path problems
- State-based artificial intelligence behavior
- Real-time simulation and game loops
- Clean, modular Python architecture

This project is well suited for:
- Computer science coursework
- Artificial intelligence demonstrations
- Game development portfolios
- Technical interviews and resume projects

---

## License

MIT License

You are free to use, modify, and distribute this project with attribution.
