# Data Structures

## 1. Data Structures and Algorithms

- **Data Structures**
    - Various structures for organizing and managing data in computers
        - Each type of data has efficient organizing rules
        - Primitive data structures: numbers, characters
        - Composite data structures: containers that store multiple data items together
    - Composite data structures
        - Linear data structures
        - Non-linear data structures

- **Algorithms**
    - A set of procedures/methods/instructions to solve a problem
        - Program = Data Structure + Algorithm
    - Algorithm requirements
        - Input: Zero or more
        - Output: One or more
        - Definiteness: Instructions are clear and unambiguous
        - Finiteness: Must terminate after a finite number of steps
        - Effectiveness: Instructions are executable
    - Algorithm description methods
        - Natural language
        - Flowchart
        - Pseudo-code
        - Programming language

- **Abstract Data Type (ADT)**
    - An abstractly defined data type
        - Only the provided data and operations are defined
        - Implementation method is not defined
        - Focuses on core structure and behavior
    - Only the interface is exposed (information hiding)
    - More suitable to implement as a class

- **Algorithm Performance**
    - Computation speed, memory usage, functionality
        - Computation speed is often prioritized
    - Measuring time is difficult
        - Implementation required
        - Use identical hardware and software environments
        - Variability depending on data

- **Complexity Analysis**
    - Analyze algorithm efficiency without actual implementation
        - Analyze how execution time increases as input size \( n \) increases
        - Evaluation method independent of hardware/software environment
    - Analyze the number of operations in the algorithm
        - Time complexity function \( T(n) \): number of operations as a function of \( n \)
    - Big O notation
        - As \( n \) increases, the highest-degree term dominates
        - Other terms are relatively ignored
        - Only the highest-degree term is considered for time complexity
    - Big Omega
        - Indicates the lower bound of a function
    - Big Theta
        - Indicates both the upper and lower bounds with the same function

- **Input Data**
    - Execution time varies depending on input data
        - Best case, average case, worst case
        - Worst-case execution time is important: air traffic control, games, robotics

---

## 2. List & Set

- **List / Linear List**
    - Linear structure where items are arranged in order
        - Each item has an order/position
    - Insertion and addition possible at any position
    - List vs. Set
        - Whether there is an order among items

- **List Implementation**
    - **Array structure**
        - Used to create data of the same type together
        - Uses index operator [ ]
        - Items are located in contiguous memory: access time complexity \( O(1) \)
        - Difficult to change capacity, inefficient for operations in the middle (insert, delete, modify)
    - **Linked structure**
        - Uses links to know the next item's location
        - No guarantee that items are in adjacent memory: access time complexity \( O(n) \)
        - Easy to change capacity, efficient for insertions and deletions

- **List Implementation Example**
    - List ADT using Python

- **List Applications**
    - Line editor
        - i: Insert line. Add a line at a given row number with a string
        - d: Delete a line. Delete the line at a given row number
        - r: Replace a line. Change the content at a given row number with a string
        - p: Print current content. Print all lines with line numbers
        - l: Load file. Read lines from a specified file (test.txt)
        - s: Save file. Save edits to a specified file (test.txt)
        - q: Exit editor

- **Set**
    - Does not allow duplicate elements
    - No order among elements

- **Set Implementation**
    - Set ADT using Python

---

## 3. Stack

- **Stack**
    - Last-In First-Out (LIFO) data structure
        - Only the top of the stack can be used for insertion and deletion
        - The top can be the front or rear of a list
    - Simpler operations than lists due to restricted input/output

- **Stack Applications**
    - "Undo" feature in document editors
    - "Back" button in web browsers
    - System stack for complex function calls
    - Source code checker (parentheses matching)
    - Calculator (expression evaluation)
    - Maze solving

- **Stack Implementation**
    - Stack ADT using Python

- **Stack Application Example**
    - Parentheses checker

---

## 4. Queue & Deque

- **Queue**
    - First-In First-Out (FIFO) data structure
    - Insertion at the rear, deletion at the front

- **Queue Applications**
    - Buffer, call queue
    - Print job queue
    - Buffering (e.g., real-time video streaming)
    - Simulation (bank queues, airport runways, network packet modeling)

- **Queue Implementation (Linear Queue)**
    - Linear queue ADT using Python

- **Queue Implementation (Circular Queue)**
    - Uses separate variables for front and rear
    - Front: index before the first element
    - Rear: index of the last element
    - Empty state: front and rear are equal
    - Full state: front % M == (rear + 1) % M
    - One space is always left empty to distinguish between full and empty
    - Circular queue ADT using Python

- **Queue Module**
    - `import queue`
    - Provides queue and stack classes

- **Queue Applications**
    - Maze search (breadth-first search)

- **Deque**
    - Double-ended queue: insertion and deletion possible at both ends
        - More flexible than stack or queue
        - Can be used as stack or queue
    - Does not allow insertion or deletion in the middle

- **Deque Implementation**
    - Deque ADT using Python

- **Deque Implementation (Circular Queue Inheritance)**
    - Deque ADT using circular queue inheritance in Python

- **Priority Queue**
    - Queue with the concept of priority
    - All data has priority; higher-priority data is output first
    - Can behave as queue or stack depending on how priority is assigned
        - If earlier items have higher priority: behaves like a queue (FIFO)
        - If earlier items have lower priority: behaves like a stack (LIFO)

- **Priority Queue Applications**
    - Simulation
    - Network traffic control
    - OS job scheduling
    - Numerical computation
    - Applications (selecting high-priority candidates)
        - Data compression: Huffman coding tree
        - Kruskal minimum spanning tree algorithm
        - Dijkstra shortest path algorithm
        - A* algorithm

- **Priority Queue Implementation (Linear Queue)**
    - Priority queue ADT using Python

- **Priority Queue Applications**
    - Strategic maze search

---

## 5. Linked Structures

- **Linked Structure**
    - Data records (nodes) linked together by references (links or pointers)
    - Increasing the number of links allows efficient representation of linear structures, trees, and graphs
    - Linked list: a connected structure that can be arranged in a line

- **Linked Structure vs. Array Structure**
    - Fixed capacity
    - Insertion and deletion of items is easier (\( O(n) \) vs \( O(1) \))
    - Accessing items (\( O(1) \) vs \( O(n) \))
    - Implementation convenience and error occurrence

- **Basic Linked List Structure**
    - Node
        - Data field: variable to store data
        - Link field: variable to store the address of another node
    - Head pointer
        - Variable to store the address of the start node
        - The last link's value is None

- **Types of Linked Lists**
    - Singly linked list: linked in one direction (one link)
    - Circular linked list: last node's link points to the first node
    - Doubly linked list: knows both previous and next nodes' links

- **Applications**
    - Linked stack (using Node class)
    - Linked list (using Node class, with getNode(pos))
    - Circular linked list: linked queue
    - Doubly linked list: linked deque

---

## 6. Sorting and Searching

- **Sorting**
    - Rearranging data in order
        - Efficient sorting requires appropriate data structures
        - Objects must be comparable by some attribute
        - Attribute can be the basis for sorting
    - Efficiency of searching can change depending on sorting
    - Ascending order, descending order

- **Sorting Definition**
    - Rearranging records in order of keys
        - Record: the object to be sorted
        - Field: various attributes a record has
        - Key / Sort key: the field used as the basis for sorting

- **Sorting Classification**
    - By sorting location
        - Internal sorting: all data is in main memory
        - External sorting: most data is on external storage, only some in memory (used for large data)
    - By implementation complexity and algorithm efficiency
        - Simple, inefficient methods: insertion sort, selection sort, bubble sort
        - Complex, efficient methods: quick sort, heap sort, merge sort, radix sort
    - By stability
        - Stability: if multiple records have the same key value, their relative order remains unchanged after sorting
        - Insertion sort, bubble sort, merge sort

- **Simple Sorting Algorithms**
    - **Selection Sort**
        - Selects the smallest number from the list and moves it to the front
        - Divides into two lists (unsorted, sorted)
        - In-place sorting: does not use additional arrays
        - Process:
            1. Select the smallest number from the unsorted list
            2. Move the selected number to the end of the sorted list
            3. Repeat steps 1-2 until the unsorted list is empty
        - Time complexity: \( O(n^2) \)
            - \( (n-1) + (n-2) + \cdots + 1 = \frac{n(n-1)}{2} = O(n^2) \)
        - Number of data moves is fixed regardless of input data

    - **Insertion Sort**
        - Repeatedly inserts a new record into the correct position in the sorted part
        - In-place sorting: does not use additional arrays
        - Process:
            1. Select the correct position for the new record
            2. Move existing records and insert the new record
            3. Repeat steps 1-2 until all records are sorted
        - Time complexity varies with input data
            - Best case: \( O(n) \)
            - Worst case: \( O(n^2) \)
        - Inefficient for large or large-sized records, efficient for small or nearly sorted data

    - **Bubble Sort**
        - Compares adjacent records and swaps them if not in order
            - After one scan, the largest record is at the end
        - In-place sorting: does not use additional arrays
        - Process:
            1. Perform compare-swap for the entire list
            2. Repeat for the remaining unsorted list
        - Time complexity: \( O(n^2) \)

- **Sorting Applications**
    - Set operations: Sorting can improve time complexity for set operations (comparison, union, difference, intersection)

- **Searching**
    - Finding something among data
        - e.g., finding a product, searching a website with words/sentences
    - Definition: finding a record with the desired search key in a table
        - Table: collection of records
        - Search key: key to distinguish records
    - Search efficiency varies with table structure
    - Map / Dictionary (e.g., Python's dict)
        - Data structure for searching
        - Collection of keyed records called entries
    - Entry
        - Key: search key to distinguish records (e.g., English word, person's name)
        - Value: value associated with the search key (e.g., meaning, address)
    - Map implementation methods
        - List: sorted/unsorted
        - Binary search tree (improves map search performance): unsorted
        - Hashing: unsorted

- **Simple Searching Algorithms**
    - **Linear Search**
        - Simplest, intuitive method
        - Applicable to unsorted tables: checks each record in order
        - Time complexity: \( O(n) \)

    - **Binary Search**
        - Suitable for sorted tables (e.g., dictionary lookup)
            1. Check the middle value to determine if the target is to the left or right
            2. Each step halves the search space
        - Not suitable for frequent insertions/deletions
        - Time complexity: \( O(\log_2 n) \)

    - **Interpolation Search**
        - Variant of binary search, suitable for sorted tables
            - Predicts the likely position of the search key
            - Divides the list unevenly based on key value
            - \[
                \text{position} = \text{low} + (\text{high} - \text{low}) \cdot \frac{k - A[\text{low}]}{A[\text{high}] - A[\text{low}]}
              \]
        - Time complexity: \( O(\log_2 \log_2 n) \)

- **Advanced Searching Algorithm: Hashing**
    - Simple search algorithms find items by comparison
        - Repeatedly compare the search key with each record's key
    - Hashing computes the address of a record using arithmetic on the key
        - Hash function: computes the address from the search key
        - Hash address: address computed by the hash function
        - Hash table: table storing records at hash addresses
    - Time complexity: \( O(1) \)
    - Collision: different keys map to the same address
        - Synonym: key causing a collision
        - If enough slots, can store in different slots
    - Overflow: more collisions than slots
    - Ideal vs. real hashing
        - Table size, memory
        - Frequent collisions, overflow
        - Often worse than \( O(1) \)
    - Linear probing for overflow
        - Check next slot until empty
    - Process:
        1. Repeat linear probing until empty slot is found
        2. If found, store the record
        3. If end of table is reached, wrap to start
        4. If back to collision point, table is full
    - Clustering: records cluster at collision points, reducing efficiency
    - Search operation: find record by hash address
    - Delete operation: can make search impossible in linear probing
    - Reducing clustering: quadratic probing, double hashing
    - Quadratic probing
    - Double hashing / rehashing: use a different hash function for collisions
    - Overflow handling: chaining (store multiple records in a bucket, implemented as a linked list)
        - Efficient in memory and speed
    - Good hash function: few collisions, evenly distributed, fast to compute
    - Examples: division method, folding, mid-square, bit extraction, number analysis, string keys
    - Performance: loading density/factor, method comparison

- **Map Applications**
    - Vocabulary book
        - Entry definition
        - Implementation: sequential search map (list), chained hash map, Python dict

---

## 7. Tree

- **Tree**
    - Hierarchical, non-linear data structure consisting of nodes connected by links
    - Used to represent hierarchical relationships

- **Tree Terminology**
    - Node, edge, root, parent, child, leaf, subtree, level, key

- **General Tree Representation**
    - Various ways to represent hierarchical relationships

- **Binary Tree**
    - Each node has at most two children

- **Types of Binary Trees**
    - Full, complete, perfect, skewed, etc.

- **Properties of Binary Trees**
    - Various mathematical properties related to nodes and structure

- **Binary Tree Representation**
    - Array-based
    - Linked-based

- **Binary Tree Operations**
    - Traversal (in-order, pre-order, post-order)
    - Level-order traversal

- **Binary Tree Implementation Example**
    - Example code for binary tree

- **Binary Tree Applications**
    - Morse code decision tree

- **Heap Tree**
    - Special binary tree for priority queues
    - Heap operations: insertion, deletion
    - Max heap, min heap
    - Used in priority queue implementation

- **Huffman Coding Tree**
    - Used for data compression
    - Built using a minimum heap

---

## 8. Search Tree

- **Search Tree**
    - Tree structure used for searching keys

- **Binary Search Tree (BST)**
    - Each node's left child has a lower value; right child has a higher value
    - Efficient for search, insert, delete operations
    - Operations: search, insert, delete
    - Performance: fast, especially in balanced trees
    - BST-based map: used for implementing map data structures
    - Balanced BST: maintains tree balance for efficient operations
    - Balanced BST operations: insert, delete, search
    - Balanced BST-based map: used for efficient map implementations

---

## 9. Graph

- **Graph**
    - Abstract data type consisting of a set of objects connected by links
    - Objects are vertices; links are edges

- **Graph Definition**
    - Represents relationships between entities

- **Types of Graphs**
    - Directed, undirected, weighted, unweighted, cyclic, acyclic

- **Graph Terminology**
    - Vertex, edge, degree, path, cycle, connected component

- **Graph Representation**
    - Adjacency matrix, adjacency list

- **Graph Traversal**
    - Depth-First Search (DFS)
    - Breadth-First Search (BFS)

- **Graph Connectivity**
    - Checking connected components

- **Spanning Tree**
    - Subset of a graph connecting all vertices without cycles

- **Topological Sorting**
    - Ordering vertices in a directed acyclic graph

---

## 10. Weighted Graph

- **Weighted Graph**
    - Graph where edges have weights (costs)

- **Weighted Graph Representation**
    - Using adjacency matrix or adjacency list

- **Minimum Spanning Tree**
    - Kruskal's algorithm
    - Prim's algorithm

- **Shortest Path**
    - Dijkstra's algorithm
    - Floyd-Warshall algorithm
