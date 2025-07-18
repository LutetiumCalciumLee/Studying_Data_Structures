# Data Structures

## Chapter 1: Data Structures and Algorithms

### Data Structure
- **Definition**: Various ways to organize and structure data in a computer
- **Purpose**: Each type of data has efficient organizing rules
- **Types**:
  - Simple data structures: numbers, characters
  - Compound data structures: containers that store multiple data items together
- **Categories**:
  - Linear data structures
  - Non-linear data structures

### Algorithm
- **Definition**: A procedure/method/set of instructions to solve a problem
- **Formula**: Program = Data Structure + Algorithm
- **Properties**:
  - Input: Zero or more inputs exist
  - Output: At least one output exists
  - Definiteness: Instructions are clear and unambiguous
  - Finiteness: Must terminate after finite steps
  - Effectiveness: Instructions are executable operations
- **Description Methods**:
  - Natural language
  - Flowchart
  - Pseudocode
  - Programming language

### Abstract Data Type (ADT)
- **Definition**: Data type defined abstractly
- **Characteristics**:
  - Only data and operations are defined
  - Implementation method is not specified
  - Focuses on core structure and behavior
- **Interface**: Only exposes the interface (information hiding)
- **Implementation**: More suitable to implement as a class

### Algorithm Performance
- **Factors**: Calculation speed, memory usage, functionality achievement
- **Priority**: Calculation speed is often prioritized
- **Measurement Challenges**:
  - Requires implementation
  - Same hardware conditions needed
  - Same software environment (compiled language > interpreted language)
  - Variable according to data

### Complexity Analysis
- **Purpose**: Analyze algorithm efficiency without actual implementation
- **Focus**: Analyze how execution time increases as input size n increases
- **Method**: Hardware and software environment independent evaluation
- **Time Complexity Function**: T(n) - number of operations as function of n
- **Big O Notation**: Only considers the highest order term as n increases
- **Big Omega (Ω)**: Indicates lower bound of function
- **Big Theta (Θ)**: Indicates both upper and lower bounds with same function

### Input Data
- **Execution Time Variation**: Depends on input data
- **Cases**:
  - Best case
  - Average case
  - Worst case
- **Importance**: Worst-case execution time is important for critical systems (aircraft control, games, robotics)

## Chapter 2: List & Set

### List / Linear List
- **Definition**: Linear data structure with items arranged in order
- **Characteristics**:
  - Items have order/position
  - Can insert and add items at arbitrary positions
- **List vs Set**: Whether there is order among items

### List Implementation Methods
- **Array Structure**:
  - Used when creating data of same type together
  - Uses index operator [ ]
  - Items in contiguous memory: O(1) access time complexity
  - Difficult to change capacity, inefficient for middle operations
- **Linked Structure**:
  - Uses links to know next item's position
  - Items not guaranteed to be in adjacent memory: O(n) access time complexity
  - Easy to change capacity, efficient insertion and deletion

### List Implementation
- Python-based List ADT implementation
- Class-based List ADT implementation

### List Applications
- **Line Editor**:
  - i: Insert line
  - d: Delete line
  - r: Replace line
  - p: Print current content
  - l: Load file
  - s: Save file
  - q: Quit editor

### Set
- **Definition**: Collection that does not allow duplicate elements
- **Characteristics**:
  - No duplicate elements allowed
  - No order among elements

### Set Implementation
- Python-based Set ADT implementation with operations:
  - union, intersect, difference, contains, insert, delete

## Chapter 3: Stack

### Stack Definition
- **Structure**: Last-In First-Out (LIFO) data structure
- **Operations**: Only insertion and deletion at the top
- **Position**: Top can be either front or back of list
- **Simplicity**: Simpler operations than lists due to restricted I/O

### Stack Applications
- Document editor "undo" function
- Web browser "back" function
- System stack for complex function calls
- Source code checking (parentheses matching)
- Calculator programs (expression evaluation)
- Maze exit finding

### Stack Implementation
- **Python-based Stack ADT**:
  - Operations: push, pop, peek, isEmpty, size, clear
  - Efficiency: Using rear of Python list is O(1), using front is O(n)

### Stack Applications
- **Parentheses Checking**: Validate matching parentheses in code
- **Expression Evaluation**: Convert infix to postfix notation
- **Maze Solving**: Depth-first search using stack

## Chapter 4: Queue & Deque

### Queue
- **Structure**: First-In First-Out (FIFO) data structure
- **Operations**: Insertion at rear, deletion at front

### Queue Applications
- Buffer, call queue
- Print job queue
- Buffering (real-time video streaming)
- Simulation (bank waiting tickets, airport runway usage, network packet modeling)

### Queue Implementation
- **Linear Queue**: Simple implementation using Python lists
- **Circular Queue**:
  - Variables: front (before first element), rear (last element index)
  - Empty state: front == rear
  - Full state: front % M == (rear + 1) % M
  - Always keep one space empty to distinguish empty and full states

### Python Queue Module
- `import queue`
- Provides Queue and Stack classes
- Queue.Queue(), Queue.LifoQueue()

### Queue Applications
- **Maze Solving**: Breadth-first search using queue

### Deque (Double-ended Queue)
- **Structure**: Queue allowing insertion and deletion at both ends
- **Flexibility**: More flexible I/O than stack or queue
- **Restriction**: Cannot insert or delete in middle

### Deque Implementation
- Inherits from circular queue
- Additional operations: addFront, deleteFront, getFront, addRear, deleteRear, getRear

### Priority Queue
- **Definition**: Queue with priority concept
- **Behavior**: Higher priority data is output first
- **Generality**: Most general queue type
- **Behavior Control**: Can behave like queue (FIFO) or stack (LIFO) based on priority assignment

### Priority Queue Applications
- Simulation
- Network traffic control
- OS task scheduling
- Numerical computation
- Applications requiring highest priority selection:
  - Data compression (Huffman coding tree)
  - Kruskal's minimum spanning tree algorithm
  - Dijkstra's shortest path algorithm
  - A* algorithm

## Chapter 5: Linked Structures

### Linked Structure
- **Definition**: Method of managing/representing scattered data by connecting with links
- **Scalability**: Increasing links allows efficient representation of linear, tree, and graph structures
- **Linked List**: Linear arrangement of linked structures

### Linked Structure vs Array Structure
- **Capacity**: Fixed (array) vs Dynamic (linked)
- **Insertion/Deletion**: O(n) (array) vs O(1) (linked)
- **Access**: O(1) (array) vs O(n) (linked)
- **Implementation**: Convenience and error occurrence differences

### Basic Linked List Structure
- **Node**:
  - Data field: variable to store data
  - Link field: variable to store address of another node
- **Head Pointer**: stores address of first node
- **Termination**: Last link value is None

### Types of Linked Lists
- **Singly Linked List**: Connected in one direction (1 link)
- **Circular Linked List**: Last node's link points to first node
- **Doubly Linked List**: Knows both previous and next node links

### Linked List Applications
- **Linked Stack**: Stack implementation using Node class
- **Linked List**: List implementation using Node class with getNode(pos) method
- **Circular Linked List**: Used for linked queue
- **Doubly Linked List**: Used for linked deque

## Chapter 6: Sorting and Searching

### Sorting
- **Definition**: Rearranging data in order
- **Requirements**: 
  - Appropriate data structure needed for efficient sorting
  - Comparable attributes needed for comparison
  - Attributes can be sorting criteria
- **Impact**: Sorting affects search efficiency
- **Orders**: Ascending order, descending order

### Sorting Definition
- **Process**: Rearranging records in key order
- **Terms**:
  - Record: object to be sorted
  - Field: attributes of record
  - Key/Sort key: attribute used as sorting criterion

### Sorting Classification
- **By Location**:
  - Internal sorting: all data in main memory
  - External sorting: most data on external storage, part in memory
- **By Complexity/Efficiency**:
  - Simple, inefficient: insertion sort, selection sort, bubble sort
  - Complex, efficient: quicksort, heap sort, merge sort, radix sort
- **By Stability**:
  - Stability: relative order of records with same key value unchanged after sorting
  - Stable: insertion sort, bubble sort, merge sort

### Simple Sorting Algorithms
- **Selection Sort**:
  - Method: Select smallest number and move to front
  - Time complexity: O(n²)
  - In-place sorting
- **Insertion Sort**:
  - Method: Insert new record in correct position in sorted part
  - Time complexity: O(n) best case, O(n²) worst case
  - In-place sorting
- **Bubble Sort**:
  - Method: Compare adjacent records and swap if out of order
  - Time complexity: O(n²)
  - In-place sorting

### Sorting Applications
- **Set Operations**: Sorting can improve time complexity for set comparison, union, difference, intersection

### Searching
- **Definition**: Finding something among data
- **Formal Definition**: Finding record with desired search key in table
- **Terms**:
  - Table: collection of records
  - Search key: key to identify records
- **Efficiency**: Table organization affects search efficiency
- **Map/Dictionary**: Data structure for searching with key-value entries

### Simple Search Algorithms
- **Sequential Search**:
  - Method: Check each record in order from beginning
  - Time complexity: O(n)
  - Works on unsorted tables
- **Binary Search**:
  - Method: Check middle value to determine which half to search
  - Time complexity: O(log₂n)
  - Requires sorted table
- **Interpolation Search**:
  - Method: Predict likely position of search key
  - Time complexity: O(log₂log₂n)
  - Variant of binary search

### Advanced Search: Hashing
- **Definition**: Uses arithmetic operations on key to compute address
- **Components**:
  - Hash function: computes storage address from key
  - Hash address: address calculated by hash function
  - Hash table: table storing records at hash addresses
- **Time Complexity**: O(1) ideal case
- **Problems**:
  - Collision: different keys map to same address
  - Overflow: more collisions than available slots
- **Collision Resolution**:
  - Linear probing: check next slots sequentially
  - Quadratic probing: use quadratic increments
  - Double hashing: use second hash function
  - Chaining: store multiple records in linked list per bucket

### Hash Function Examples
- **Division method**: h(k) = k % M (M is prime)
- **Folding method**: for large keys
- **Mid-square method**: use middle bits of squared key
- **Bit extraction method**
- **Digit analysis method**
- **String hashing**: convert characters to integers

### Map Applications
- **Dictionary**: Entry definition with key-value pairs
- **Implementation methods**:
  - Sequential search map using lists
  - Hash map using chaining
  - Python dictionary implementation

## Chapter 7: Tree

### Tree
- **Definition**: Data structure suitable for representing hierarchical data
- **Examples**: Organization chart, family tree, computer folder structure
- **Applications**:
  - Search tree (searching)
  - Heap tree (priority queue)
  - Decision tree (decision structure)
- **Recursive Definition**: Trees are defined recursively

### Tree Terminology
- **Root node**: Highest node in hierarchical structure
- **Edge**: Line connecting nodes
- **Parent/Child node**: Upper/lower nodes directly connected by edge
- **Sibling node**: Nodes with same parent
- **Ancestor/Descendant node**: Nodes on path to root / all nodes below
- **Terminal/Leaf node**: Node with no children
- **Degree of node**: Number of children a node has
- **Degree of tree**: Largest node degree in tree
- **Level**: Layer number (root is level 1, increases downward)
- **Height of tree**: Maximum level in tree
- **Forest**: Collection of trees

### General Tree Representation
- **General Tree**: Tree where nodes can have arbitrary number of children
- **Representation**: Usually linked structure with data field and child links
- **Simplification**: Use two links (child, sibling) for uniform representation

### Binary Tree
- **Definition**: Tree where every node has at most two subtrees
- **Properties**:
  - Recursively defined
  - Subtrees can be empty
  - Maximum 2 children per node
  - Children are ordered (left, right)

### Binary Tree Types
- **Full Binary Tree**: Every level completely filled
- **Complete Binary Tree**: All levels filled except possibly last (filled left to right)

### Binary Tree Properties
- n nodes → n-1 edges
- Height k → at most 2^k - 1 nodes
- n nodes → height between ⌈log₂(n+1)⌉ and n

### Binary Tree Representation
- **Array Representation**:
  - Allocate array of size 2^k - 1
  - Use full binary tree numbering as indices
  - Good for full/complete trees, wasteful for skewed trees
- **Linked Representation**:
  - Each node has two links (left, right child)
  - More flexible but requires more complex management

### Binary Tree Traversal
- **Preorder (VLR)**: Root → Left subtree → Right subtree
- **Inorder (LVR)**: Left subtree → Root → Right subtree
- **Postorder (LRV)**: Left subtree → Right subtree → Root
- **Level-order**: Visit nodes level by level using queue

### Binary Tree Operations
- **Node counting**: Count all nodes recursively
- **Leaf counting**: Count nodes with no children
- **Height calculation**: Find maximum depth

### Binary Tree Applications
- **Morse Code Decision Tree**: 
  - Encoding: alphabet → Morse code (O(1))
  - Decoding: Morse code → alphabet using decision tree (O(log n))

### Heap Tree
- **Definition**: Complete binary tree based data structure
- **Purpose**: Quickly find largest (or smallest) value
- **Types**:
  - Max heap: parent key ≥ child key
  - Min heap: parent key ≤ child key
- **Operations**:
  - Insert: O(log₂n) - sift-up process
  - Delete: O(log₂n) - sift-down process
- **Representation**: Array is most efficient
- **Applications**: Priority queue implementation

### Huffman Coding Tree
- **Purpose**: Variable-length coding based on frequency
- **Principle**: High frequency items get shorter bit codes
- **Construction**: Use min heap to build tree from bottom up
- **Efficiency**: More efficient than fixed-length ASCII codes

## Chapter 8: Search Tree

### Search Tree
- **Purpose**: Tree-based data structure for efficient searching
- **Advantage**: Overcomes limitations of existing search methods

### Binary Search Tree (BST)
- **Definition**: Binary tree for efficient searching (O(log₂n))
- **Properties**:
  - All nodes have unique keys
  - Left subtree keys  root key
  - Both subtrees are also BSTs
- **Advantage**: Maintains sorted state by definition

### BST Operations
- **Search by Key**: O(log₂n) average case
  - Compare key with root
  - Go left if key  root
- **Search by Value**: O(n) - must check all nodes
- **Min/Max Search**: Follow leftmost/rightmost path
- **Insert**: O(log₂n) - follow search path, insert at failure point
- **Delete**: Most complex operation with 3 cases:
  - Case 1: Leaf node - simply remove
  - Case 2: One child - connect child to parent
  - Case 3: Two children - replace with successor

### BST Performance
- **Tree Shape Dependent**: Performance varies with tree structure
- **Balanced Tree**: O(log₂n) for all operations
- **Skewed Tree**: O(n) for all operations (worst case)

### Balanced Binary Search Tree (AVL Tree)
- **Purpose**: Guarantee balanced tree for consistent O(log₂n) performance
- **Balance Factor**: Height difference between left and right subtrees
- **Constraint**: Balance factor must be -1, 0, or 1
- **Rebalancing**: Use rotations when balance factor becomes ±2
- **Rotation Types**:
  - Single rotation: LL, RR
  - Double rotation: LR, RL
- **Insert Operation**: Insert then rebalance from inserted node up to root

## Chapter 9: Graph

### Graph
- **Definition**: Data structure representing relationships between connected objects
- **Versatility**: Most generalized data structure (can represent linear structures, trees)
- **Applications**: Subway maps, flight routes, social networks, computer networks

### Graph Definition
- **Notation**: G = (V, E)
  - G: graph
  - V(G): set of vertices/nodes
  - E(G): set of edges/links
- **Representation**: Pairs of vertices, e.g., (A, B)

### Graph Types
- **Undirected Graph**: Edges have no direction (bidirectional)
- **Directed Graph**: Edges have direction (unidirectional)
- **Weighted Graph**: Edges have costs or weights
- **Subgraph**: Graph formed by subset of vertices and edges

### Graph Terminology
- **Adjacent Vertex**: Vertices directly connected by edge
- **Degree**: Number of edges connected to vertex
- **Path**: Sequence of vertices connected by edges
- **Simple Path**: Path with no repeated edges
- **Cycle**: Path where start and end vertices are same
- **Connected Graph**: Graph where path exists between all vertex pairs
- **Complete Graph**: Graph with edges between all vertex pairs
- **Tree**: Connected graph with no cycles

### Graph Representation
- **Adjacency Matrix**: n×n matrix representing connections
  - Advantages: O(1) edge lookup, suitable for dense graphs
  - Disadvantages: O(n²) space regardless of edge count
- **Adjacency List**: List of adjacent vertices for each vertex
  - Advantages: O(n+e) space, suitable for sparse graphs
  - Disadvantages: O(degree) edge lookup time

### Graph Traversal
- **Depth-First Search (DFS)**:
  - Strategy: Go deep first, backtrack when stuck
  - Implementation: Use stack or recursion
  - Applications: Connected components, topological sort
- **Breadth-First Search (BFS)**:
  - Strategy: Visit nearby vertices first
  - Implementation: Use queue
  - Applications: Shortest path, level-order traversal

### Graph Applications
- **Connected Component Detection**: Find separate connected parts
- **Spanning Tree**: Tree connecting all vertices with n-1 edges
- **Topological Sort**: Order vertices respecting dependencies (DAG only)


## Chapter 10: Weighted Graph

### Weighted Graph

### Weighted Graph Representation

### Minimum Spanning Tree (MST)

### MST Algorithms

### Shortest Path

### Shortest Path Algorithms

### Algorithm Comparison
