Graph-Traversal
Graph overview
Edge list : {0, 1}, {0, 2}, {1, 3}, {1, 4}, {2, 5}, {2, 6}, {3, 5}

DFS
Depth-First Search explores as far as possible along each branch before backtracking. A stack is used to manage the traversal order.

Iterative:
Use a stack, mark the starting node as visited, and push it onto the stack.
While the stack is not empty:
Pop a node, process it, and push its unvisited neighbors.
Recursive:
Process the node, mark it as visited, and recurse into its unvisited neighbors.
Result 0 -> 1 -> 3 -> 5 -> 2 -> 6 -> 4

BFS
BFS explores the graph level by level. It uses a queue to traverse all neighbors of a node before moving to the next level.

Create a queue and mark the starting node as visited.
Enqueue the starting node.
While the queue is not empty:
Dequeue a node, process it, and enqueue its unvisited neighbors.
Result 0 -> 1 -> 2 -> 3 -> 4 -> 5 -> 6

Observations and Insights
Traversal in DFS The DFS traversal order can vary depending on the adjacency list order (which determines the neighbor visit order). In this case, we observe different DFS orders based on whether we visit 3 or 4 first, and similarly for 5.

Traversal in BFS The BFS traversal order remains consistent as it explores level by level. However, BFS results may differ if we have different starting points or graph structures.

Performance Both algorithms operate in O(V + E) time complexity, where:

V is the number of vertices.
E is the number of edges.
Cycle Detection Cycles in the graph were managed efficiently by maintaining a visited list.

Graph Properties The graph's small size made it suitable for demonstrating traversal techniques. The presence of cycles showcased the need for proper visited node management.
