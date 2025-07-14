# Beam Search Algorithm Implementation in C++

## Overview

This program implements the **Beam Search** algorithm, a heuristic search strategy used to explore a graph or tree by expanding the most promising nodes first. It is particularly useful in scenarios where the number of possible paths is very large, and a full search is impractical.

## What is Beam Search?

Beam search works by:

*   Starting with an initial node.
*   At each step, generating all possible next nodes (or a subset) and evaluating them based on a heuristic.
*   Selecting a fixed number (`beam_width`) of the best candidates to continue exploring.
*   Repeating this process until the goal is reached or no more nodes can be explored.

Unlike exhaustive search algorithms (like BFS or DFS), beam search trades completeness for efficiency by pruning less promising paths.

## Code Structure

### Functions

1.  `main()`:
    *   Takes user input for: number of nodes (`n`), number of edges (`e`), heuristic values, graph connections, start node, goal node, and beam width.
    *   Builds the graph as an adjacency list.
    *   Performs beam search and prints the result.


## Sample Execution

This example uses a graph with **6 nodes** and **7 edges**, with a beam width of **2**.

![Image](https://github.com/user-attachments/assets/8b445290-b582-4e04-8f71-e87871ead8c5)

### Explanation

*   The heuristic values guide the search: lower values are preferred.
*   The beam width of 2 limits exploration to the top 2 candidates at each step.
*   The algorithm finds the goal node **5** efficiently by pruning less promising paths.

## Complexity

*   **Time Complexity**: O(b^L), where b is the branching factor, and L is the depth of the search. The beam width can significantly reduce the number of nodes evaluated.
*   **Space Complexity**: O(b*L), as the algorithm needs to store the nodes at each level.

## Applications

1.  **Machine Translation**: Beam search is used in machine translation systems to find the best translation by exploring multiple possible translations.
2.  **Speech Recognition**: It is used in speech recognition systems to find the most likely transcription of a spoken sentence.
3.  **Natural Language Processing**: Beam search can be used in NLP tasks such as parsing, named entity recognition, and text summarization.

## Advantages

1.  **Efficiency**: Beam search is more efficient than exhaustive search algorithms, making it suitable for large graphs or trees.
2.  **Flexibility**: It can be used with different heuristics and beam widths to trade off between efficiency and accuracy.

## Disadvantages

1.  **Completeness**: Beam search does not guarantee finding the optimal solution, as it prunes less promising paths.
2.  **Heuristic Quality**: The performance of beam search depends on the quality of the heuristic function.

## How it Works

1.  **Initialization**: The algorithm starts with an initial node and a beam width.
2.  **Node Evaluation**: The algorithm evaluates all possible next nodes based on a heuristic.
3.  **Beam Selection**: The algorithm selects the top `beam_width` nodes to continue exploring.
4.  **Iteration**: The algorithm repeats steps 2-3 until the goal is reached or no more nodes can be explored.

## License

This project is open-source—feel free to use, modify, or distribute it.
