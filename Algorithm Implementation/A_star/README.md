# A* Search Algorithm Implementation in C++

## Overview

This program implements the **A\* Search** algorithm, a popular pathfinding method that finds the shortest path from a start node to a goal node in a weighted graph. It combines Dijkstra's algorithm with heuristics to guide the search efficiently toward the goal.

## What is A\* Search?

A\* is an informed search algorithm that uses:

*   **g(n)**: The actual cost from the start node to the current node `n`.
*   **h(n)**: A heuristic estimate of the cost from `n` to the goal (must be admissible, i.e., never overestimate).
*   **f(n) = g(n) + h(n)**: The total estimated cost, used to prioritize nodes.

The algorithm explores nodes with the lowest `f(n)` first, using a priority queue, and stops when the goal is reached or no path exists.

## Code Structure

### Functions

1.  `a_star_search(unordered_map<int, vector<pair<int, int>>>& graph, int start, int goal, unordered_map<int, int>& heuristic)`:
    *   Performs the A\* search on the graph.
    *   Uses a priority queue to select the next node based on `f(n)`.
    *   Tracks `g_values` for actual costs and reconstructs the path.
    *   Returns the path as a vector of nodes if found; otherwise, an empty vector.
2.  `main()`:
    *   Takes user input for: number of nodes, heuristic values, number of edges, graph direction (undirected/directed), edges with costs, start node, and goal node.
    *   Builds the graph as an adjacency list.
    *   Calls `a_star_search()` and prints the result.

## How it Works

1.  **Initialization**: The algorithm starts by initializing the `g_values` and priority queue with the start node.
2.  **Node Selection**: The node with the lowest `f(n)` is selected from the priority queue.
3.  **Goal Check**: If the selected node is the goal, the algorithm reconstructs the path and returns it.
4.  **Neighbor Exploration**: The algorithm explores the neighbors of the selected node, updates their `g_values` and `f(n)` values, and adds them to the priority queue if necessary.

## Complexity

*   **Time Complexity**: O(b^d), where b is the branching factor and d is the depth of the search.
*   **Space Complexity**: O(b^d), as in the worst case, the algorithm may need to store all nodes at a given depth.

## Applications

1.  **Pathfinding**: A\* Search is widely used in video games, robotics, and logistics for finding the shortest path between two points.
2.  **Network Routing**: It is used in network routing protocols to find the optimal path for data transmission.
3.  **Resource Allocation**: A\* Search can be used to optimize resource allocation in complex systems.
![Image](https://github.com/user-attachments/assets/0a4ff9aa-4c64-4071-8870-a8047aaa3bfb)
## Advantages

1.  **Optimality**: A\* Search guarantees finding the optimal solution if the heuristic is admissible and consistent.
2.  **Efficiency**: It is more efficient than uninformed search algorithms like BFS and DFS, especially in large graphs.

## Disadvantages

1.  **Heuristic Quality**: The performance of A\* Search heavily depends on the quality of the heuristic function.
2.  **Computational Cost**: The algorithm can be computationally expensive for very large graphs.

## Example Use Cases

1.  **Video Games**: A\* Search is used in video games to implement pathfinding for characters and NPCs.
2.  **Autonomous Vehicles**: It is used in autonomous vehicles to plan optimal routes and avoid obstacles.
3.  **Logistics and Supply Chain Management**: A\* Search can be used to optimize routes for delivery trucks and reduce transportation costs.

## License

This project is open-source—feel free to use, modify, or distribute it.

