# Depth-First Search (DFS) Algorithm Implementation in C++

## Overview

This program implements the **Depth-First Search (DFS)** algorithm, a graph traversal strategy that explores as far as possible along each branch before backtracking. It is particularly useful for finding connected components, testing whether a graph is connected, and solving mazes.

## What is DFS?

DFS works by:

*   Starting with an initial node (or root node).
*   Exploring as far as possible along each branch before backtracking.
*   Using a stack data structure (or recursion) to keep track of the nodes to be visited.

## Code Structure

### Functions

1.  `dfs(int V, int root)`:
    *   Performs the DFS traversal on the graph.
    *   Uses a boolean array to track visited nodes.
    *   Prints the visited nodes.

2.  `main()`:
    *   Takes user input for: number of vertices, number of edges, graph connections, and root node.
    *   Builds the graph as an adjacency matrix.
    *   Calls `dfs()` and prints the result.

## Sample Execution

This example uses a graph with **6 vertices** and **7 edges**.

![Image](https://github.com/user-attachments/assets/401d237e-e9d2-45e0-a88a-450136be286e)
### Explanation

*   The algorithm starts at node **0** and explores as far as possible along each branch before backtracking.
*   The visited nodes are printed in the order they are traversed.

## Complexity

*   **Time Complexity**: O(V + E), where V is the number of vertices, and E is the number of edges.
*   **Space Complexity**: O(V), as the algorithm needs to store the visited nodes.

## Applications

1.  **Graph Traversal**: DFS is used in graph traversal problems, such as finding connected components.
2.  **Network Analysis**: It is used in network analysis to find strongly connected components.
3.  **Maze Solving**: DFS can be used to solve mazes.

## Advantages

1.  **Efficiency**: DFS is efficient for finding connected components in a graph.
2.  **Simplicity**: It is a simple algorithm to implement.

## Disadvantages

1.  **Not Suitable for Finding Shortest Paths**: DFS is not suitable for finding the shortest path in a graph.
2.  **Space Requirements**: The algorithm requires significant space to store the visited nodes.

## How it Works

1.  **Initialization**: The algorithm starts with an initial node and a boolean array to track visited nodes.
2.  **Node Exploration**: The algorithm explores as far as possible along each branch.
3.  **Backtracking**: The algorithm backtracks when it reaches a dead end.

## License

This project is open-source—feel free to use, modify, or distribute it.
