# Minimax Algorithm Implementation

## Overview

The Minimax algorithm is a recursive algorithm used for decision making in games like chess, checkers, and other two-player games. It considers the current state of the game and the possible moves from that state, evaluating the best move by considering the opponent's possible responses.

## How it Works

1.  **Initialization**: The algorithm starts with the current state of the game.
2.  **Evaluation**: The algorithm evaluates the current state and determines if it's a winning, losing, or neutral state.
3.  **Recursion**: The algorithm recursively explores all possible moves from the current state, considering the opponent's possible responses.

## Code Structure

### Functions

1.  `minimax(int depth, int index, bool is_max, const vector<int>& scores, int h)`:
    *   Recursively traverses the game tree and applies the Minimax algorithm.
    *   `depth`: Current depth in the tree.
    *   `index`: Index of the current node.
    *   `is_max`: `true` if the current node is a maximizing node; `false` if it's a minimizing node.
    *   `h`: Height of the tree (number of levels from the root to a leaf).
    *   Returns the best value the maximizing player can guarantee.


## Sample Execution

This example uses a game tree of height **2** with leaf node values `[5, 6, 7, 4]`.
![Image](https://github.com/user-attachments/assets/a54d6747-5201-460b-a7a4-4258830bbcbd)
### Explanation

*   The algorithm evaluates the game tree and determines the best value the maximizing player can guarantee.

## Complexity

*   **Time Complexity**: O(b^d), where b is the branching factor, and d is the depth of the tree.
*   **Space Complexity**: O(d), as the algorithm needs to store the nodes at each level.

## Applications

1.  **Game Playing**: The Minimax algorithm is widely used in game-playing AI, such as chess, checkers, and other two-player games.
2.  **Decision Making**: It is used in decision-making systems to evaluate the best course of action.

## Advantages

1.  **Optimality**: The Minimax algorithm guarantees finding the optimal solution if the evaluation function is accurate.
2.  **Efficiency**: It is more efficient than exhaustive search algorithms for large game trees.

## Disadvantages

1.  **Complexity**: Implementing the Minimax algorithm can be complex, especially for large game trees.
2.  **Evaluation Function**: The performance of the Minimax algorithm depends on the quality of the evaluation function.

## License

This project is open-source—feel free to use, modify, or distribute it.
