# Bidirectional Search Algorithm Implementation in C++

## Overview

This program implements the **Bidirectional Search** algorithm, a graph search strategy that uses two simultaneous searches: one from the start node and one from the goal node. The algorithm terminates when the two searches meet in the middle, reducing the search space and improving efficiency.

## What is Bidirectional Search?

Bidirectional search works by:

*   Performing two simultaneous searches: one from the start node and one from the goal node.
*   At each step, exploring the neighbors of the current nodes in both searches.
*   Terminating when the two searches meet in the middle, indicating a path has been found.

## Code Structure

### Functions

1.  `bidirectional_search(vector<vector<int>> &graph, int start, int goal)`:
    *   Performs the bidirectional search on the graph.
    *   Uses two queues and two sets to track visited nodes.
    *   Returns `true` if a path is found; otherwise, `false`.

2.  `main()`:
    *   Takes user input for: number of nodes, number of edges, graph connections, start node, and goal node.
    *   Builds the graph as an adjacency list.
    *   Calls `bidirectional_search()` and prints the result.

## How to Compile and Run

### Prerequisites

*   A C++ compiler (e.g., **g++**) installed on your system.

### Steps

1.  Save the code as `bidirectional_search.cpp`.
2.  Open a terminal/command prompt and navigate to the directory where the file is saved.
3.  Compile the code:
    ```bash
g++ bidirectional_search.cpp -o bidirectional_search
```
4.  Run the executable:
    ```bash
./bidirectional_search
```

## Sample Execution

This example uses a graph with **6 nodes** and **7 edges**.
![Image](https://github.com/user-attachments/assets/20d24326-ca45-43f2-a62d-719e4d7b6880)
### Explanation

*   The algorithm performs two simultaneous searches: one from node **0** and one from node **5**.
*   The searches meet at node **2** or **4**, indicating a path has been found.

## Complexity

*   **Time Complexity**: O(b^(d/2)), where b is the branching factor, and d is the depth of the search. Bidirectional search can significantly reduce the search space compared to unidirectional search.
*   **Space Complexity**: O(b^(d/2)), as the algorithm needs to store the nodes at each level.

## Applications

1.  **Graph Search**: Bidirectional search is used in graph search problems, such as finding the shortest path between two nodes.
2.  **Network Routing**: It is used in network routing protocols to find the optimal path for data transmission.
3.  **Game Playing**: Bidirectional search can be used in game-playing AI to evaluate game states and make moves.

## Advantages

1.  **Efficiency**: Bidirectional search can significantly reduce the search space, making it more efficient than unidirectional search.
2.  **Scalability**: It is suitable for large graphs or networks.

## Disadvantages

1.  **Complexity**: Implementing bidirectional search can be complex, especially for large graphs.
2.  **Meeting Point**: The algorithm may not always find the optimal meeting point.

## How it Works

1.  **Initialization**: The algorithm starts with two queues and two sets to track visited nodes.
2.  **Node Exploration**: The algorithm explores the neighbors of the current nodes in both searches.
3.  **Termination**: The algorithm terminates when the two searches meet in the middle.

## License

This project is open-source—feel free to use, modify, or distribute it.
