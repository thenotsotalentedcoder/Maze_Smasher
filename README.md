# Maze Smasher 🎮

A sophisticated 2D maze game built in Unity that showcases advanced pathfinding algorithms and dynamic gameplay mechanics. The game features three distinct modes, each demonstrating different aspects of algorithmic pathfinding and game AI.

## 🎯 Game Modes

### 1. Algorithm Visualizer Mode
Experience and compare three popular pathfinding algorithms in action:

- **A* Algorithm**
  - Combines path cost and heuristic estimation
  - Optimized for finding the shortest path efficiently
  - Visualizes both exploration and final path
  
- **Dijkstra's Algorithm**
  - Guarantees the shortest path through systematic exploration
  - Explores all possible paths methodically
  - Perfect for understanding exhaustive path searching
  
- **Breadth-First Search (BFS)**
  - Explores the maze level by level
  - Demonstrates basic graph traversal concepts
  - Efficient for finding paths in simpler mazes

Features:
- Real-time visualization of algorithm exploration
- Color-coded path display
- Dynamic maze generation using DFS
- Reset functionality for new maze generation
- Step-by-step algorithm progression

### 2. Player vs AI Race Mode
Challenge yourself against increasingly sophisticated AI opponents in a competitive race through randomly generated mazes:

Features:
- Randomly generated mazes using custom DFS algorithm
- Two challenging stages:
  - Stage 1: Race against an AI using Dijkstra's algorithm
  - Stage 2: Unlocked after beating Stage 1 - Face a more efficient AI using A* algorithm
- Real-time competitive gameplay
- Smooth player movement system
- Progressive difficulty system
- End-point detection for winner determination

### 3. Player vs Enemy Mode
A challenging survival maze adventure where players must collect stars while avoiding or confronting intelligent enemies:

Features:
- **Core Gameplay**:
  - Collect 3 stars scattered throughout the maze to unlock the finish path
  - Navigate carefully while avoiding or confronting enemies
  - Strategic combat system with sword attacks
  - 3 lives system - lose all lives and it's game over

- **Enemy AI**:
  - Intelligent enemies using A* pathfinding algorithm
  - Real-time pursuit of the player
  - Dynamic threat assessment
  - Strategic positioning and attack patterns

- **Combat System**:
  - Sword-based combat mechanics
  - Tactical engagement opportunities
  - Defensive positioning requirements
  - Risk-reward decision making

## 🎮 How to Play

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/thenotsotalentedcoder/Maze_Smasher.git
   ```
2. Open in Unity (Version 6 or later)
3. Build and run the game

### Controls

#### Algorithm Visualizer Mode
- Use mouse to select the desired pathfinding algorithm
- Click "Reset" button to generate a new random maze
- Click "Exit" button to return to main menu

#### Player vs AI Race Mode
- Move using WASD or Arrow keys
- Note: If you restart in Stage 2, you'll need to beat Stage 1 again
- Use "Exit" button to return to main menu

#### Player vs Enemy Mode
- Move using WASD or Arrow keys
- Use mouse to aim the direction of your sword (left or right)
- Right-click to swing sword and attack enemies
- You have 3 lives - be careful!

## 🔧 Technical Implementation

### Core Systems

#### 1. Maze Generation System
- **Algorithm**: Depth-First Search (DFS) with backtracking
- **Features**:
  - Guaranteed solvability
  - Random maze layout generation
  - Multiple path generation for complexity
  - Perfect maze structure (no loops)

#### 2. Grid System
- **Data Structure**: 2D Boolean Arrays
  - Walls array: Tracks maze structure
  - Visited array: Manages exploration
- **Node Properties**:
  - Position (x, y)
  - Walkability status
  - Cost values (g-cost, h-cost, f-cost)

#### 3. Pathfinding Implementation

##### A* Algorithm
- Uses a combination of actual distance (g-cost) and estimated distance to target (h-cost)
- Maintains two lists: open set (nodes to explore) and closed set (explored nodes)
- Prioritizes nodes with lowest total cost (f-cost = g-cost + h-cost)
- Efficiently finds optimal path by exploring most promising nodes first
- Uses parent references to reconstruct the final path
- More efficient than Dijkstra's for directed searches due to heuristic guidance

##### Dijkstra's Algorithm Implementation
- Priority queue-based exploration
- Systematic node evaluation
- Optimal path guarantee

##### BFS Implementation
- Queue-based level traversal
- Complete path exploration
- Memory-efficient implementation

## 🔍 Future Enhancements

1. Technical Improvements
   - Dynamic obstacle implementation
   - Multi-threading for pathfinding
   - Advanced AI behaviors
   - Path smoothing algorithms

2. Gameplay Features
   - Additional game modes
   - Multiplayer support
   - Custom maze editor
   - Achievement system


## 👥 Authors

- **Malik Muzammil** - Game mode 1 (Race Mode)
- **Saim & Abdul Rehman** - Ganme mode 3 (Player vs Enemy)
- **Muhammad Taha** - Game mode 1 (Visualizer)
