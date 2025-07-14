# Beam Search Algorithm Implementation in C++

This program implements the **Beam Search** algorithm, a heuristic search strategy used to explore a graph or tree by expanding the most promising nodes first. It is particularly useful in scenarios where the number of possible paths is very large, and a full search is impractical.


## What is Beam Search?
Beam search works by:
- Starting with an initial node.
- At each step, generating all possible next nodes (or a subset) and evaluating them based on a heuristic.
- Selecting a fixed number (`beam_width`) of the best candidates to continue exploring.
- Repeating this process until the goal is reached or no more nodes can be explored.

Unlike exhaustive search algorithms (like BFS or DFS), beam search trades completeness for efficiency by pruning less promising paths.


## Code Structure

### Functions
1. `main()`:
   - Takes user input for: number of nodes (`n`), number of edges (`e`), heuristic values, graph connections, start node, goal node, and beam width.
   - Builds the graph as an adjacency list.
   - Performs beam search and prints the result.

## How to Compile and Run

### Prerequisites
- A C++ compiler (e.g., **g++**) installed on your system.

### Steps
1. Save the code as `beam_search.cpp`.
2. Open a terminal/command prompt and navigate to the directory where the file is saved.
3. Compile the code:
   ```bash
   g++ beam_search.cpp -o beam_search
   ```
4. Run the executable:
   ```bash
   ./beam_search
   ```

## Sample Execution
This example uses a graph with **6 nodes** and **7 edges**, with a beam width of **2**.
![Image](https://github.com/user-attachments/assets/ace4faa5-e470-47c6-8da0-2dd8a50804a8)

### Input
```
6 7
10 8 5 7 2 0
0 1
0 2
1 3
2 3
2 4
4 5
3 5
0 5 2
```

### Output
```
Goal: 5
Process returned 0 (0x0)  execution time : 44.090 s
Press any key to continue.
```

### Explanation
- The heuristic values guide the search: lower values are preferred.
- The beam width of 2 limits exploration to the top 2 candidates at each step.
- The algorithm finds the goal node **5** efficiently by pruning less promising paths.

## Notes
- The graph is represented as an adjacency list.
- The heuristic values are used to rank nodes at each step.
- Beam search does not guarantee finding the optimal solution but is much faster for large graphs.

## License
This project is open-source—feel free to use, modify, or distribute it.
