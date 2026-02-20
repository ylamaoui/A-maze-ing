DESCRIPTION
A-MAZE-ING is a maze generation and solving project that explores graph traversal algorithms, grid-based structures, and visualization techniques.

The project focuses on:

- Generating a maze by carving walls inside a structured grid

- Ensuring reproducibility using a seed-based random generator

- Solving the maze using a shortest-path algorithm

- Exporting the maze structure in hexadecimal format

- Providing a visual representation of the maze (ASCII or graphical rendering)

A maze is internally represented as a grid of interconnected cells, where each cell contains four possible walls (North, East, South, West). By selectively removing walls, a valid maze structure is created.

The project highlights algorithmic thinking, clean architecture design, and separation of concerns between logic and rendering.

INSTRUCTIONS
To run the project, a Makefile is provided with the following rules:

-   make run
    Builds and runs the program to generate and display the maze.

-   make install
    Installs required dependencies.

-   make lint
    Runs static analysis tools (e.g., mypy, flake8) to ensure code quality and compliance wit
    style guidelines.

-   make debug
    Launches the program in debug mode using pdb.

ALGORITHMS

Several algorithms are commonly used in maze generation. In this project, the following are 
implemented:

- Maze Generation
Depth-First Search (DFS – Recursive Backtracking)

    + Starts from a random cell

    + Visits unvisited neighbors randomly

    +Removes the wall between cells

    +Backtracks when reaching a dead end

    +Produces a perfect maze (one unique path between any two cells)

Prim’s Algorithm (Randomized Version)

    + Starts from a random cell

    + Adds its neighbors to a frontier list

    + Randomly selects a frontier cell

    + Connects it to an already visited cell

    +Continues until no frontier remains

Both algorithms generate connected maze structures.

- Maze Solving
Breadth-First Search (BFS)

    + Explores neighbors level by level

    + Expands uniformly from the starting point

    + Stops when the exit is found

    + Guarantees the shortest path

BFS is used because it ensures minimal path length between entry and exit.

-VISUALIZATION

The maze can be rendered using:

    +ASCII terminal rendering

    +MLX graphical rendering

In the graphical version (MLX):

    -A window is created

    -Walls, paths, and cells are drawn using pixel manipulation

    -Colors can be applied dynamically

    -Interactive controls may allow toggling path visibility or regenerating the maze

Visualization is separated from maze logic to maintain modularity and reusability.

-RESOURCES

🤖 AI USAGE DISCLOSURE

Artificial intelligence was used for:

    -Concept clarification

    -README structure improvement

    -Grammar and formatting correction
