# Alpha-Beta Pruning Implementation in C++

This program implements the **Alpha-Beta Pruning** algorithm—an optimization of the Minimax algorithm—for searching game trees. It reduces the number of nodes evaluated by "pruning" branches that cannot impact the final decision, making the search more efficient.


## What is Alpha-Beta Pruning?
Alpha-Beta pruning is a search algorithm that minimizes redundant computations in the Minimax algorithm (used for turn-based games). It uses two values:
- `alpha`: The best (highest) value the *maximizing player* can guarantee at the current level or above.
- `beta`: The best (lowest) value the *minimizing player* can guarantee at the current level or above.

If `beta ≤ alpha` at any node, the current branch is **pruned** (no further evaluation is needed), as it cannot improve the final result.


## Code Structure

### Functions
1. `evaluate(int node_index, const vector<int>& scores)`:
   - Returns the score of a *leaf node* (leaf nodes store the "value" of a game state).

2. `alpha_beta(int depth, int node_index, bool is_max, const vector<int>& scores, int h, int alpha, int beta)`:
   - Recursively traverses the game tree and applies Alpha-Beta pruning.
   - `depth`: Current depth in the tree.
   - `node_index`: Index of the current node (using an array to represent the tree; the left child of node `i` is `2*i + 1`, and the right child is `2*i + 2`).
   - `is_max`: `true` if the current node is a *maximizing node*; `false` if it’s a *minimizing node*.
   - `h`: Height of the tree (number of levels from the root to a leaf).
   - `alpha`, `beta`: The alpha and beta values for pruning.

3. `main()`:
   - Takes user input for the tree’s height and leaf node values.
   - Calls `alpha_beta()` to compute the optimal value and prints the result.


## How to Compile and Run

### Prerequisites
- A C++ compiler (e.g., **g++**) installed on your system.


### Steps
1. Save the code as `alpha_beta_pruning.cpp`.
2. Open a terminal/command prompt and navigate to the directory where the file is saved.
3. Compile the code:
   ```bash
   g++ alpha_beta_pruning.cpp -o alpha_beta_pruning
   ```
4. Run the executable:
   ```bash
   ./alpha_beta_pruning
   ```


## Sample Execution
Let’s test the program with a game tree of **height 3** (this means there are \(2^3 = 8\) leaf nodes).

![Image](https://github.com/user-attachments/assets/d952fd79-6c9e-4393-9cb7-59b6db764c37)
### Input
```
Enter height of the game tree: 3
Enter 8 leaf node values:
3 5 6 9 1 2 0 -1
```

### Output
```
Optimal value with alpha-beta pruning: 5
Process returned 0 (0x0)  execution time : 4.969 s
Press any key to continue.
```

### Explanation
For a tree of height 3:
- Level 0: Root node (maximizing).
- Level 1: Two minimizing nodes.
- Level 2: Four maximizing nodes.
- Level 3: Eight leaf nodes `[3, 5, 6, 9, 1, 2, 0, -1]`.

The algorithm prunes unnecessary branches and returns the best value the maximizing player can guarantee (**5** in this case).


## Notes
- The code assumes a **binary game tree** (each node has exactly 2 children).
- Leaf nodes are stored in a 1D vector: the left child of a node at index `i` is `2*i + 1`, and the right child is `2*i + 2`.
- `h` refers to the *height of the tree* (e.g., a tree with a root and leaf nodes has height 1; a tree with root → level 1 → leaf nodes has height 2).


## License
This project is open-source—feel free to use, modify, or distribute it.
