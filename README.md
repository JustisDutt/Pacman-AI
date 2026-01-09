
# AI‑Driven Pac‑Man

## Overview
This project is an AI‑controlled Pac‑Man game implemented in Python using Pygame. The core objective is to demonstrate practical pathfinding and decision‑making algorithms operating in a real‑time game environment rather than a static or turn‑based simulation.

The Pac‑Man agent uses heuristic search to navigate the maze, avoid ghosts, and prioritize pellet collection, achieving a high win rate during testing.

---

## Problem Statement
Classic Pac‑Man is a constrained, grid‑based environment that is well‑suited for search algorithms. Many AI examples stop at isolated pathfinding demos. This project focuses on **integrating AI decision logic directly into a running game loop**, where the agent must continuously re‑evaluate its strategy in response to dynamic threats.

---

## System Architecture

**High‑level flow:**
1. The game loop updates the environment state.
2. The AI agent evaluates the current grid and ghost positions.
3. A* pathfinding computes the optimal movement direction.
4. Heuristics balance pellet distance against ghost proximity.
5. The renderer updates the game state visually in real time.

**Core components:**
- **Game Logic:** Movement rules, collision detection, scoring
- **AI Engine:** A* search with heuristic evaluation
- **Rendering Layer:** Pygame‑based visualization
- **Configuration:** Centralized constants for grid and timing

---

## Tech Stack

- **Language:** Python
- **AI / Algorithms:** A* pathfinding, heuristic evaluation
- **Game Framework:** Pygame
- **Data Structures:** Grids, priority queues
- **Tooling:** Git

---

## Scope and Constraints

**In Scope**
- Single‑agent Pac‑Man AI
- Grid‑based maze navigation
- Real‑time decision making
- Deterministic ghost movement

**Out of Scope**
- Reinforcement learning
- Multi‑agent training
- Adaptive difficulty
- Networked or multiplayer support

The scope is intentionally limited to highlight algorithmic clarity and real‑time integration.

---

## Repository Structure

```
Pacman-AI/
├── main.py            # Game entry point
├── game_logic.py      # Core game rules and state updates
├── rendering.py       # Pygame rendering layer
├── constants.py       # Game configuration and constants
├── requirements.txt
└── README.md
```

---

## Running the Project Locally

### Requirements
- Python 3.9+
- Pygame

### Setup
```bash
pip install -r requirements.txt
python main.py
```

---

## What This Project Demonstrates

- Practical application of A* search in a live environment
- Heuristic‑based decision making under time constraints
- Clean separation of game logic, AI logic, and rendering
- Translating algorithm theory into interactive software

---

## Author
**Justis Dutt**  
- Portfolio: https://www.justisdutt.com  
- GitHub: https://github.com/JustisDutt  
- LinkedIn: https://www.linkedin.com/in/justis-dutt-951834224/

---
