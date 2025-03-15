**I. Foundations of Data Structures**

*   Understanding Abstract Data Types (ADTs)
    *   Defining ADTs: Concepts of data and operations.
    *   Examples: Lists, Stacks, Queues.
*   Arrays
    *   Understanding array implementation and memory allocation.
    *   Static vs. Dynamic arrays.
    *   Operations: Accessing, inserting, deleting elements.
*   Linked Lists
    *   Singly Linked Lists: Structure and Traversal.
    *   Doubly Linked Lists: Structure and Bi-directional Traversal.
    *   Circular Linked Lists: Structure and Use Cases.
    *   Operations: Insertion, Deletion, Searching.
*   Stacks
    *   LIFO (Last-In, First-Out) principle.
    *   Implementation using arrays and linked lists.
    *   Operations: `push`, `pop`, `peek`, `isEmpty`.
    *   Applications: Expression evaluation, function call management.
*   Queues
    *   FIFO (First-In, First-Out) principle.
    *   Implementation using arrays and linked lists.
    *   Operations: `enqueue`, `dequeue`, `peek`, `isEmpty`.
    *   Circular Queues: Efficient implementation for fixed-size queues.
    *   Applications: Task scheduling, breadth-first search.

**II. Trees**

*   Binary Trees
    *   Understanding tree terminology: root, node, leaf, parent, child, subtree.
    *   Types of binary trees: Complete, full, perfect.
    *   Binary Tree traversals: Inorder, Preorder, Postorder. Implement each recursively and iteratively.
*   Binary Search Trees (BSTs)
    *   Understanding BST properties: ordering of nodes.
    *   Operations: Insertion, Deletion, Searching.
    *   Time complexity analysis of BST operations.
*   Balanced Trees
    *   AVL Trees: Understanding balance factors and rotations.
    *   Red-Black Trees: Understanding color properties and rotations.
    *   B-Trees: Understanding the structure and usage for disk-based storage.
*   Heaps
    *   Understanding heap properties: min-heap, max-heap.
    *   Binary Heaps: Implementation using arrays.
    *   Operations: `insert`, `deleteMin`/`deleteMax`, `heapify`.
    *   Applications: Priority queues, heap sort.

**III. Hash Tables**

*   Understanding Hash Functions
    *   Properties of a good hash function: uniform distribution, low collision.
    *   Common hash functions: division method, multiplication method.
*   Collision Resolution Techniques
    *   Separate Chaining: Implementation using linked lists.
    *   Open Addressing: Linear probing, quadratic probing, double hashing.
*   Hash Table Operations
    *   `insert`, `delete`, `search`.
    *   Load factor and its impact on performance.
    *   Resizing hash tables.

**IV. Graphs**

*   Graph Representations
    *   Adjacency Matrix: Representation and Space Complexity.
    *   Adjacency List: Representation and Space Complexity.
*   Graph Traversal Algorithms
    *   Breadth-First Search (BFS): Implementation and Applications.
    *   Depth-First Search (DFS): Implementation and Applications.
*   Shortest Path Algorithms
    *   Dijkstra's Algorithm: For single-source shortest paths in weighted graphs (non-negative weights).
    *   Bellman-Ford Algorithm: For single-source shortest paths in weighted graphs (handling negative weights).
    *   Floyd-Warshall Algorithm: For all-pairs shortest paths.
*   Minimum Spanning Tree Algorithms
    *   Prim's Algorithm: Implementation and Time Complexity.
    *   Kruskal's Algorithm: Implementation and Time Complexity.
*   Directed Acyclic Graphs (DAGs)
    *   Topological Sorting: Algorithms and Applications.

**V. Sorting Algorithms**

*   Comparison-Based Sorting
    *   Bubble Sort: Implementation and Time Complexity.
    *   Insertion Sort: Implementation and Time Complexity.
    *   Selection Sort: Implementation and Time Complexity.
    *   Merge Sort: Divide and conquer approach, implementation, and time complexity.
    *   Quick Sort: Divide and conquer approach, pivot selection strategies, implementation, and time complexity.
    *   Heap Sort: Implementation using heaps and time complexity.
*   Non-Comparison-Based Sorting
    *   Counting Sort: Implementation and Use Cases.
    *   Radix Sort: Implementation and Use Cases.
    *   Bucket Sort: Implementation and Use Cases.
*   Sorting Algorithm Analysis
    *   Best-case, average-case, and worst-case time complexity.
    *   Space complexity.
    *   Stability of sorting algorithms.

**VI. Algorithm Design Techniques**

*   Divide and Conquer
    *   Concept and application in algorithms like Merge Sort and Quick Sort.
    *   Master Theorem for analyzing divide and conquer algorithms.
*   Greedy Algorithms
    *   Concept and application in algorithms like Dijkstra's Algorithm and Kruskal's Algorithm.
    *   Activity Selection Problem.
    *   Fractional Knapsack Problem.
*   Dynamic Programming
    *   Concept of overlapping subproblems and optimal substructure.
    *   Memoization vs. Tabulation.
    *   Examples: Fibonacci sequence, knapsack problem (0/1), longest common subsequence.
*   Backtracking
    *   Concept and application in solving constraint satisfaction problems.
    *   Examples: N-Queens problem, Sudoku solver.

**VII. Advanced Data Structures (Optional)**

*   Tries
    *   Structure and Applications.
    *   Implementation of `insert`, `search`, and `delete`.
*   Segment Trees
    *   Structure and Applications for range queries.
    *   Implementation of range minimum/maximum query and update operations.
*   Fenwick Trees (Binary Indexed Trees)
    *   Structure and Applications for prefix sum queries.
    *   Implementation of `update` and `query` operations.

**VIII. Algorithm Analysis**

*   Asymptotic Notation
    *   Big O notation: Upper bound on time complexity.
    *   Big Omega notation: Lower bound on time complexity.
    *   Big Theta notation: Tight bound on time complexity.
*   Recurrence Relations
    *   Solving recurrence relations using substitution, iteration, and master theorem.
*   Amortized Analysis
    *   Understanding aggregate analysis, accounting method, and potential method.
    *   Example: Analyzing the cost of dynamic array resizing.
