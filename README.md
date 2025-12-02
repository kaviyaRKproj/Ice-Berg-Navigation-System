# Ice-Berg-Navigation-System

Here is a complete description and a GitHub-ready README.md for your Iceberg Navigation System project.

Iceberg Navigation System: Pathfinding for Maritime Safety 🚢
This project implements an Iceberg Detection and Navigation System designed to enhance maritime safety by automatically calculating the safest and most efficient path for a ship through iceberg-laden waters. It integrates computer vision concepts (simulated here with a binary matrix) and the A* pathfinding algorithm to provide real-time navigation guidance.

Key Features
🧊 Ice Hazard Modeling: The navigation environment (an aerial image) is modeled as a grid, where regions containing icebergs are designated as obstacles.

🗺️ Optimal Pathfinding with A*: The A* search algorithm finds the shortest path from a fixed starting point (the ship's current location) to a user-defined destination, intelligently avoiding all detected ice obstacles.

🎮 Interactive Visualization: A Pygame interface allows for real-time visualization of the calculated path and an interactive environment where users can click to set new destinations and immediately see the recalculated route.

💻 Core Algorithms: The project demonstrates practical applications of pathfinding and matrix manipulation in a real-world scenario.

🛠️ Project Structure and Files
File/Directory	Description
Iceberg.ipynb	The main Jupyter Notebook containing all the Python code for grid generation, A* pathfinding logic, and the interactive Pygame visualization loop.
frame1.png	The aerial image used as the background/map for the navigation system.
selection.png	Image asset used to highlight the currently selected destination cell in the visualization.
matrix (Simulated)	Conceptual representation of the navigation grid where 1 indicates a navigable path (water) and 0 indicates an obstacle (iceberg).
⚙️ Dependencies
This project requires the following Python libraries:

pygame: Used for creating the interactive graphical interface.

pathfinding: Provides the highly optimized A* algorithm implementation.

numpy: Used for efficient numerical operations and matrix handling.

opencv-python (cv2): Used for image loading and conversion (BGR to RGB).

Installation
You can install the required dependencies using pip:

Bash
pip install pygame pathfinding numpy opencv-python
▶️ Usage
Run the Project: Open and run the Iceberg.ipynb file in a Jupyter Notebook environment (like VS Code or Jupyter Lab).

Locate the Visualization: Once the last code cell runs successfully, a Pygame window will open displaying the satellite image and the ship's environment.

Interactive Navigation:

Set Destination: Left-click anywhere on the navigable blue water area of the map to set a new destination. The system will instantly calculate and draw the shortest, safest path around the icebergs.

Clear Path: Press the Spacebar key to clear the currently displayed path.

Note: The ship's starting position is fixed at the matrix coordinates (18,12), which corresponds to a safe area on the map, ready to navigate.

💡 Algorithm Deep Dive
The core intelligence of this system lies in the A* search algorithm.

Heuristic (h): The estimated cost from the current node to the end node, calculated using the Manhattan Distance (non-diagonal movement cost).

Cost to Start (g): The actual cost from the starting node to the current node. Since movement is grid-based (up, down, left, right), each step has a uniform cost of 1.

Total Cost (f): The sum of the movement cost and the heuristic: f(n)=g(n)+h(n)

The algorithm prioritizes paths that minimize this total estimated cost, guaranteeing the optimal (shortest) path while strictly avoiding cells in the matrix marked with a 0 (iceberg obstacles).
