# A* Search Algorithm Implementation in C++

This program implements the **A* Search** algorithm, a popular pathfinding method that finds the shortest path from a start node to a goal node in a weighted graph. It combines Dijkstra's algorithm with heuristics to guide the search efficiently toward the goal.


## What is A* Search?
A* is an informed search algorithm that uses:
- **g(n)**: The actual cost from the start node to the current node `n`.
- **h(n)**: A heuristic estimate of the cost from `n` to the goal (must be admissible, i.e., never overestimate).
- **f(n) = g(n) + h(n)**: The total estimated cost, used to prioritize nodes.

The algorithm explores nodes with the lowest `f(n)` first, using a priority queue, and stops when the goal is reached or no path exists.


## Code Structure

### Functions
1. `a_star_search(unordered_map<int, vector<pair<int, int>>>& graph, int start, int goal, unordered_map<int, int>& heuristic)`:
   - Performs the A* search on the graph.
   - Uses a priority queue to select the next node based on `f(n)`.
   - Tracks `g_values` for actual costs and reconstructs the path.
   - Returns the path as a vector of nodes if found; otherwise, an empty vector.

2. `main()`:
   - Takes user input for: number of nodes, heuristic values, number of edges, graph direction (undirected/directed), edges with costs, start node, and goal node.
   - Builds the graph as an adjacency list.
   - Calls `a_star_search()` and prints the result.


## How to Compile and Run

### Prerequisites
- A C++ compiler (e.g., **g++**) installed on your system.


### Steps
1. Save the code as `a_star_search.cpp`.
2. Open a terminal/command prompt and navigate to the directory where the file is saved.
3. Compile the code:
   ```bash
   g++ a_star_search.cpp -o a_star_search
   ```
4. Run the executable:
   ```bash
   ./a_star_search
   ```


## Sample Execution
This example uses a graph with 5 nodes and 6 undirected edges.

![Image](https://github.com/user-attachments/assets/0a4ff9aa-4c64-4071-8870-a8047aaa3bfb)

### Input
```
Enter number of nodes: 5
Enter heuristic values for each node:
Node 1: 1 10
Node 2: 2 8
Node 3: 3 5
Node 4: 4 7
Node 5: 5 0
Enter number of edges: 6
Is the graph undirected? (1 for Yes, 0 for No): 1
Enter edges with cost (format: from to cost):
1 2 1
1 3 4
2 3 2
2 4 5
3 5 3
4 5 1
Enter start node: 1
Enter goal node: 5
```

### Output
```
A* Path from 1 to 5: 1 2 3 5 
Process returned 0 (0x0)   execution time : 6.962 s
Press any key to continue.
```

### Explanation
- Nodes: 1 (start) to 5 (goal).
- Heuristics guide the search (e.g., h(5) = 0 since it's the goal).
- The algorithm finds the path `1 → 2 → 3 → 5` as the optimal route based on costs and heuristics.


## Notes
- The graph is represented as an `unordered_map` of adjacency lists with pairs (neighbor, cost).
- Supports both directed (undirected=0) and undirected (undirected=1) graphs.
- Node labels are integers; ensure they match inputs.
- If no path exists, it outputs "No path found".


## License
This project is open-source—feel free to use, modify, or distribute it.

