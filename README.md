# Ice-Berg-Navigation-System

This project implements an **Iceberg Detection and Navigation System** designed to guide ships safely through waters contaminated with ice hazards. It combines image processing (simulated via a predefined binary matrix) for obstacle detection with the classic **A* pathfinding algorithm** to determine the optimal route.

## Features

* **Iceberg Detection**: Uses image processing and a predefined grid/matrix to identify and mark obstacles (icebergs) in the navigation path.
* **Optimal Pathfinding**: Implements the **A\* algorithm** to calculate the safest and most efficient path from the ship's starting point to a destination, automatically avoiding ice hazards.
* **Interactive Visualization**: Features a real-time graphical interface using Pygame for visualizing the navigation path within the grid system.
* **User Interaction**: Allows users to dynamically set a new destination using a mouse click.

## Tech Stack

| Technology | Purpose |
| :--- | :--- |
| **Python** | Core programming language for algorithm implementation and logic. |
| **Jupyter Notebook** | Development environment where the detection and navigation code resides (`Iceberg.ipynb`). |
| **Pygame** | Used for creating the interactive GUI and handling real-time visualization. |
| **Pathfinding Library** | Provides the underlying implementation of the A\* pathfinding algorithm. |

## Project Structure

* `Iceberg.ipynb`: The main notebook containing the code for image processing, grid definition, the A\* implementation, and the Pygame visualization loop.
* `frame1.png`: The image asset used as the background/map for the system.
* `selection.png`: A small graphic used for visual representation, typically to highlight the selected destination cell.
* `matrix`: A conceptual data structure (implemented as a NumPy array in Python) representing the navigation grid, where `1` is a clear path (water) and `0` is an obstacle (iceberg).

## Installation

To set up the project and run it locally, you need Python and the required libraries.

1.  **Clone the Repository (Replace with your actual URL):**
    ```bash
    git clone [YOUR_REPO_URL]
    cd Ice-Berg-Navigation-System
    ```

2.  **Install Dependencies:**
    The project relies on `pygame` and `pathfinding` (along with `numpy` and `opencv-python`).

    ```bash
    pip install pygame pathfinding numpy opencv-python
    ```

## Usage

1.  **Run the Notebook**: Open and execute the cells in the `Iceberg.ipynb` file within a Jupyter environment.
2.  **Start Navigation**: A Pygame window will appear displaying the environment. The ship's predefined starting position is at cell coordinates **(18, 12)**.
3.  **Set Destination**:
    * **Left-click** anywhere on the navigable area of the map (where there are no icebergs) to set a new destination.
    * The system will instantly calculate and display the optimal path avoiding all obstacles.
4.  **Clear Path**:
    * Press the **Space** key to clear the current navigation path.

---
