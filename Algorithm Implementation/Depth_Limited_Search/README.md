# Depth-Limited Search (DLS) Algorithm Implementation in C++

## Overview

This program implements the **Depth-Limited Search (DLS)** algorithm, a graph traversal strategy that explores a graph or tree by expanding the most promising nodes first, with a limited depth. It is particularly useful in scenarios where the number of possible paths is very large, and a full search is impractical.

## What is DLS?

DLS works by:

*   Starting with an initial node.
*   Exploring as far as possible along each branch up to a specified depth limit.
*   Backtracking when the depth limit is reached.

## Code Structure

### Functions

1.  `DLS(const vector<vector<int>> &graph, int current, int goal, int limit, vector<bool> &visited)`:
    *   Performs the DLS traversal on the graph.
    *   Uses a boolean array to track visited nodes.
    *   Prints the visited nodes.

2.  `main()`:
    *   Takes user input for: number of nodes, number of edges, graph connections, start node, goal node, and depth limit.
    *   Builds the graph as an adjacency list.
    *   Calls `DLS()` and prints the result.

## Sample Execution

This example uses a graph with **6 nodes** and **7 edges**, with a depth limit of **3**.
![Image](https://github.com/user-attachments/assets/54b118eb-2ab4-4ec0-9bc0-486afc04f191)
### Explanation

*   The algorithm starts at node **0** and explores as far as possible along each branch up to a depth of **3**.
*   The goal node **5** is found within the specified depth limit.

## Complexity

*   **Time Complexity**: O(b^L), where b is the branching factor, and L is the depth limit.
*   **Space Complexity**: O(L), as the algorithm needs to store the nodes at each level.

## Applications

1.  **Graph Traversal**: DLS is used in graph traversal problems, such as finding connected components.
2.  **Network Analysis**: It is used in network analysis to find nodes within a certain distance.
3.  **Game Playing**: DLS can be used in game-playing AI to evaluate game states and make moves.

## Advantages

1.  **Efficiency**: DLS is more efficient than exhaustive search algorithms, making it suitable for large graphs or trees.
2.  **Flexibility**: It can be used with different depth limits to trade off between efficiency and accuracy.

## Disadvantages

1.  **Incomplete**: DLS may not find a solution if the goal node is beyond the specified depth limit.
2.  **Heuristic Quality**: The performance of DLS depends on the quality of the heuristic function.

## How it Works

1.  **Initialization**: The algorithm starts with an initial node and a depth limit.
2.  **Node Exploration**: The algorithm explores as far as possible along each branch up to the depth limit.
3.  **Backtracking**: The algorithm backtracks when it reaches a dead end or the depth limit.

## License

This project is open-source—feel free to use, modify, or distribute it.
