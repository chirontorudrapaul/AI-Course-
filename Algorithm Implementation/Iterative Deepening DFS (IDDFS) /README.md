# Iterative Deepening Depth-First Search (IDDFS) Algorithm Implementation in C++

## Overview

This program implements the **Iterative Deepening Depth-First Search (IDDFS)** algorithm, a graph traversal strategy that combines the benefits of Breadth-First Search (BFS) and Depth-First Search (DFS). It is particularly useful for finding the shortest path in an unweighted graph.

## What is IDDFS?

IDDFS works by:

*   Performing a series of depth-limited searches with increasing depth limits.
*   Starting with a depth limit of 0 and incrementing it until the goal node is found.

## Code Structure

### Functions

1.  `DLS(vector<vector<int>> &graph, int src, int goal, int limit, vector<bool> &visited)`:
    *   Performs a depth-limited search on the graph.
    *   Uses a boolean array to track visited nodes.

2.  `IDS(vector<vector<int>> &graph, int src, int goal, int max_depth)`:
    *   Performs the IDDFS traversal on the graph.
    *   Calls `DLS()` with increasing depth limits until the goal node is found.

3.  `main()`:
    *   Takes user input for: number of nodes, number of edges, graph connections, start node, and goal node.
    *   Builds the graph as an adjacency list.
    *   Calls `IDS()` and prints the result.



## Sample Execution

This example uses a graph with **6 nodes** and **7 edges**.
![Image](https://github.com/user-attachments/assets/052194af-580a-49f6-b004-ee8bb1481fb9)
### Explanation

*   The algorithm performs a series of depth-limited searches with increasing depth limits.
*   The goal node **5** is found at a depth of **3**.

## Complexity

*   **Time Complexity**: O(b^d), where b is the branching factor, and d is the depth of the goal node.
*   **Space Complexity**: O(d), as the algorithm needs to store the nodes at each level.

## Applications

1.  **Graph Traversal**: IDDFS is used in graph traversal problems, such as finding connected components.
2.  **Network Analysis**: It is used in network analysis to find nodes within a certain distance.
3.  **Game Playing**: IDDFS can be used in game-playing AI to evaluate game states and make moves.

## Advantages

1.  **Efficiency**: IDDFS is more efficient than exhaustive search algorithms, making it suitable for large graphs or trees.
2.  **Optimality**: It guarantees finding the shortest path to the goal node.

## Disadvantages

1.  **Incomplete**: IDDFS may not find a solution if the goal node is not reachable.
2.  **Heuristic Quality**: The performance of IDDFS depends on the quality of the heuristic function.

## How it Works

1.  **Initialization**: The algorithm starts with an initial node and a maximum depth.
2.  **Depth-Limited Search**: The algorithm performs a depth-limited search on the graph.
3.  **Incrementing Depth Limit**: The algorithm increments the depth limit until the goal node is found.

## License

This project is open-source—feel free to use, modify, or distribute it.
