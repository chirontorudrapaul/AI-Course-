# Alpha-Beta Pruning Algorithm Implementation in C++

## Overview

This program implements the **Alpha-Beta Pruning** algorithm, an optimization of the Minimax algorithm, for searching game trees. It reduces the number of nodes evaluated by "pruning" branches that cannot impact the final decision, making the search more efficient.

## What is Alpha-Beta Pruning?

Alpha-Beta pruning is a search algorithm that minimizes redundant computations in the Minimax algorithm (used for turn-based games). It uses two values:

*   **alpha**: The best (highest) value the maximizing player can guarantee at the current level or above.
*   **beta**: The best (lowest) value the minimizing player can guarantee at the current level or above.

If `beta ≤ alpha` at any node, the current branch is pruned (no further evaluation is needed), as it cannot improve the final result.

## Code Structure

### Functions

1.  `evaluate(int node_index, const vector<int>& scores)`:
    *   Returns the score of a leaf node (leaf nodes store the "value" of a game state).
2.  `alpha_beta(int depth, int node_index, bool is_max, const vector<int>& scores, int h, int alpha, int beta)`:
    *   Recursively traverses the game tree and applies Alpha-Beta pruning.
    *   `depth`: Current depth in the tree.
    *   `node_index`: Index of the current node (using an array to represent the tree; the left child of node `i` is `2*i + 1`, and the right child is `2*i + 2`).
    *   `is_max`: `true` if the current node is a maximizing node; `false` if it’s a minimizing node.
    *   `h`: Height of the tree (number of levels from the root to a leaf).
    *   `alpha`, `beta`: The alpha and beta values for pruning.
3.  `main()`:
    *   Takes user input for the tree’s height and leaf node values.
    *   Calls `alpha_beta()` to compute the optimal value and prints the result.

## How it Works

1.  **Initialization**: The algorithm starts by initializing the alpha and beta values.
2.  **Node Evaluation**: The algorithm evaluates the current node and its children.
3.  **Pruning**: If `beta ≤ alpha`, the current branch is pruned.
4.  **Recursion**: The algorithm recursively explores the game tree.

## Complexity

*   **Time Complexity**: O(b^(h/2)), where b is the branching factor and h is the height of the tree. Alpha-Beta pruning can significantly reduce the number of nodes evaluated compared to the Minimax algorithm.
*   **Space Complexity**: O(h), as the maximum depth of the recursion tree.

## Applications

1.  **Game Playing**: Alpha-Beta pruning is widely used in game-playing AI, such as chess, checkers, and Go.
2.  **Decision Making**: It is used in decision-making systems to optimize the search for the best course of action.
3.  **Resource Allocation**: Alpha-Beta pruning can be used to optimize resource allocation in complex systems.
**SAMPLE input Output**
![Image](https://github.com/user-attachments/assets/d952fd79-6c9e-4393-9cb7-59b6db764c37)

## Advantages

1.  **Efficiency**: Alpha-Beta pruning can significantly reduce the number of nodes evaluated, making the search more efficient.
2.  **Optimality**: It guarantees finding the optimal solution if the evaluation function is accurate.

## Disadvantages

1.  **Complexity**: Implementing Alpha-Beta pruning can be complex, especially for large game trees.
2.  **Heuristic Quality**: The performance of Alpha-Beta pruning depends on the quality of the evaluation function.

## Example Use Cases

1.  **Chess Engines**: Alpha-Beta pruning is used in chess engines to evaluate positions and make moves.
2.  **Game Development**: It is used in game development to implement AI opponents.
3.  **Resource Optimization**: Alpha-Beta pruning can be used to optimize resource allocation in complex systems.

## License

This project is open-source—feel free to use, modify, or distribute it.

