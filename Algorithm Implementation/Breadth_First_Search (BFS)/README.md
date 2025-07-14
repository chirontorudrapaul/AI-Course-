# Breadth-First Search (BFS) Algorithm Implementation in C++

## Overview

This program implements the **Breadth-First Search (BFS)** algorithm, a graph traversal strategy that explores all the nodes at a given depth level before moving on to the next level. It is particularly useful for finding the shortest path in an unweighted graph.

## What is BFS?

BFS works by:

*   Starting with an initial node (or root node).
*   Exploring all of its neighbors at the present depth prior to moving on to nodes at the next depth level.
*   Using a queue data structure to keep track of the nodes to be visited.

## Code Structure

### Functions

1.  `bfs(int no_vertices, int root)`:
    *   Performs the BFS traversal on the graph.
    *   Uses a queue and an array to track visited nodes.
    *   Prints the visited nodes.

2.  `main()`:
    *   Takes user input for: number of vertices, number of edges, graph connections, and root node.
    *   Builds the graph as an adjacency matrix.
    *   Calls `bfs()` and prints the result.


## Sample Execution

This example uses a graph with **6 vertices** and **7 edges**.
![Image](https://github.com/user-attachments/assets/501a46bc-47d5-43ed-8df7-69e0181ebdad)
### Explanation

*   The algorithm starts at node **0** and explores all its neighbors at each depth level.
*   The visited nodes are printed in the order they are traversed.

## Complexity

*   **Time Complexity**: O(V + E), where V is the number of vertices, and E is the number of edges.
*   **Space Complexity**: O(V), as the algorithm needs to store the visited nodes.

## Applications

1.  **Graph Traversal**: BFS is used in graph traversal problems, such as finding connected components.
2.  **Network Analysis**: It is used in network analysis to find the shortest path between two nodes.
3.  **Web Crawling**: BFS can be used in web crawling to traverse the web graph.

## Advantages

1.  **Efficiency**: BFS is efficient for finding the shortest path in an unweighted graph.
2.  **Simplicity**: It is a simple algorithm to implement.

## Disadvantages

1.  **Not Suitable for Weighted Graphs**: BFS is not suitable for finding the shortest path in a weighted graph.
2.  **Space Requirements**: The algorithm requires significant space to store the visited nodes.

## How it Works

1.  **Initialization**: The algorithm starts with an initial node and a queue.
2.  **Node Exploration**: The algorithm explores all the neighbors of the current node.
3.  **Queue Operations**: The algorithm uses queue operations (enqueue and dequeue) to manage the nodes to be visited.

## License

This project is open-source—feel free to use, modify, or distribute it.
