# Greedy Hill Climbing Algorithm

## Overview

Greedy Hill Climbing is a heuristic search algorithm used to find a peak or optimum in a graph or landscape defined by heuristic values. It is a simple, efficient algorithm that iteratively moves to the neighbor with the best (lowest) heuristic value until no better neighbor can be found.

## How it Works

1. **Initialization**: Start at an initial node.
2. **Evaluation**: Evaluate all neighbors of the current node.
3. **Selection**: Select the neighbor with the best (lowest) heuristic value.
4. **Iteration**: Repeat steps 2-3 until no better neighbor can be found.

## Complexity

* **Time Complexity**: O(b^d), where b is the branching factor and d is the depth of the search.
* **Space Complexity**: O(b^d), as in the worst case, the algorithm may need to store all nodes at a given depth.

## Applications

1. **Optimization Problems**: Greedy Hill Climbing is used to find optimal solutions in problems such as scheduling, resource allocation, and logistics.
2. **Machine Learning**: It is used in machine learning to optimize model parameters and find the best configuration.
3. **Computer Networks**: Greedy Hill Climbing is used in computer networks to optimize routing and resource allocation.
4. **Robotics**: It is used in robotics to optimize motion planning and control.
   
**SAMPLE input & Output**
![Image](https://github.com/user-attachments/assets/98e18237-d1b9-4dd4-afe9-73965a7aed75)

## Advantages

1. **Efficient**: Greedy Hill Climbing is an efficient algorithm that can find a good solution quickly.
2. **Simple**: It is a simple algorithm to implement and understand.
3. **Flexible**: Greedy Hill Climbing can be used in a variety of problems and domains.

## Disadvantages

1. **Local Optima**: Greedy Hill Climbing can get stuck in local optima, which may not be the global optimum.
2. **No Guarantee**: There is no guarantee that the algorithm will find the global optimum.

## Example Use Cases

1. **Traveling Salesman Problem**: Greedy Hill Climbing can be used to find a good solution for the traveling salesman problem.
2. **Resource Allocation**: It can be used to optimize resource allocation in a manufacturing system.
3. **Motion Planning**: Greedy Hill Climbing can be used to optimize motion planning in robotics.

## Code Explanation

The provided C++ code implements the Greedy Hill Climbing algorithm to find a peak in a graph defined by heuristic values. The code takes user input for the number of nodes, heuristic values, graph connections, and start node, and then performs the algorithm to find the peak.

## License

This project is open-source—feel free to use, modify, or distribute it.
