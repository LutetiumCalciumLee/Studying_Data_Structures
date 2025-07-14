# Data Structures

## 1. Data Structures and Algorithms

- **Data Structure**
    - Various ways to organize and structure data in a computer.
        - Each type of data has efficient organizing rules.
        - *Simple data structures*: numbers, characters
        - *Compound data structures*: containers that store multiple data items together
    - Compound data structures:
        - Linear data structures
        - Non-linear data structures

- **Algorithm**
    - A procedure/method/set of instructions to solve a problem.
        - Program = Data Structure + Algorithm
    - Algorithm properties:
        - Input: Zero or more inputs
        - Output: At least one output
        - Definiteness: Each instruction is clear and unambiguous
        - Finiteness: Must terminate after a finite number of steps
        - Effectiveness: Instructions are executable
    - Algorithm description methods:
        - Natural language
        - Flowchart
        - Pseudocode
        - Programming language

- **Abstract Data Type (ADT)**
    - Data type defined abstractly
        - Only the data and operations provided are defined
        - Implementation method is not specified
        - Focuses on core structure and behavior
    - Only the interface is exposed (information hiding)
    - More suitable to implement as a class

- **Algorithm Performance**
    - Calculation speed, memory usage, functionality
        - Calculation speed is often prioritized
    - Measuring time is difficult:
        - Requires implementation
        - Use the same hardware and software environment
        - Implementation language (compiled > interpreted)
        - Varies depending on input data

- **Complexity Analysis**
    - Analyze algorithm efficiency without actual implementation
        - Analyze how execution time increases as input size $$ n $$ increases
        - Evaluation method independent of hardware/software environment
    - Analyze the number of operations in the algorithm
        - Time complexity function $$ T(n) $$: number of operations as a function of $$ n $$
    - **Big O notation**
        - As $$ n $$ increases, the highest order term dominates
        - Lower order terms are ignored
        - Only the highest order term of the time complexity function is considered
    - **Big Omega ($$\Omega$$)**
        - Indicates the lower bound of a function
    - **Big Theta ($$\Theta$$)**
        - Indicates both the upper and lower bounds with the same function

- **Input Data**
    - Execution time varies by input data
        - Best case, average case, worst case
        - Worst-case execution time is important (e.g., air traffic control, games, robotics)

## 2. List & Set

- **List / Linear List**
    - Linear data structure where items are arranged in order
        - Each item has an order/position
    - Items can be inserted or added at arbitrary positions
    - List vs Set
        - Whether there is an order among items

- **List Implementation Methods**
    - **Array structure**
        - Used when creating data of the same type together
        - Uses index operator [ ]
        - Items are in contiguous memory: access time complexity $$ O(1) $$
        - Difficult to change capacity; inefficient for operations in the middle (add, delete, modify)
    - **Linked structure**
        - Uses links to know the next item's position
        - Items may not be in adjacent memory: access time complexity $$ O(n) $$
        - Easy to change capacity; efficient for insertion and deletion

- **List Applications**
    - **Line Editor**
        - i: Insert a line at a specified line number
        - d: Delete a line at a specified line number
        - r: Replace a line at a specified line number
        - p: Print all lines with line numbers
        - l: Load lines from a specified file (e.g., test.txt)
        - s: Save lines to a specified file (e.g., test.txt)
        - q: Quit the editor

- **Set**
    - Does not allow duplicate elements
    - No order among elements

## 3. Stack

- **Stack**
    - Last-In First-Out (LIFO) data structure
        - Insertion and deletion only at the top
        - The top can be either the front or back of a list
    - Simpler operations than lists due to restricted input/output

- **Stack Applications**
    - Undo function in document editors
    - "Back" function in web browsers
    - System stack (complex function call relationships)
    - Source code checking (parentheses matching)
    - Calculator (expression evaluation)
    - Maze exit finding

## 4. Queue & Deque

- **Queue**
    - First-In First-Out (FIFO) data structure
    - Insertion at the rear, deletion at the front

- **Queue Applications**
    - Buffer, call queue
    - Print job queue
    - Buffering (e.g., real-time video streaming)
    - Simulation (bank waiting tickets, airport runway usage, network packet modeling)

- **Queue Implementation (Linear Queue)**
    - Uses front and rear variables

- **Queue Implementation (Circular Queue)**
    - Front: index before the first element
    - Rear: index of the last element
    - Empty state: front and rear are equal
    - Full state: $$ \text{front} \% M == (\text{rear} + 1) \% M $$
    - Always keep one space empty to distinguish empty and full states

- **Deque**
    - Double-ended queue: insertion and deletion at both ends
        - More flexible than stack or queue
        - Cannot insert or delete in the middle

- **Priority Queue**
    - Queue with priority concept
    - Each data item has a priority; higher priority items are output first
    - Can behave like a queue (FIFO) or stack (LIFO) depending on priority assignment

- **Priority Queue Applications**
    - Simulation
    - Network traffic control
    - OS task scheduling
    - Numerical computation
    - Applications: Huffman coding tree, Kruskal's MST algorithm, Dijkstra's shortest path, A* algorithm

## 5. Linked Structures

- **Linked Structure**
    - Method of managing/representing scattered data by connecting them with links
        - Increasing the number of links allows efficient representation of linear, tree, and graph structures
    - **Linked list**: a linear arrangement of linked nodes

- **Linked Structure vs Array Structure**
    - Fixed capacity (array)
    - Insertion/deletion efficiency: $$ O(n) $$ (array) vs $$ O(1) $$ (linked)
    - Access efficiency: $$ O(1) $$ (array) vs $$ O(n) $$ (linked)
    - Implementation convenience and error occurrence

- **Basic Structure of Linked List**
    - **Node**
        - Data field: variable to store data
        - Link field: variable to store the address of another node
    - **Head pointer**
        - Stores the address of the first node
        - Last link is None

- **Types of Linked Lists**
    - Singly linked list: nodes connected in one direction (one link)
    - Circular linked list: last node's link points to the first node
    - Doubly linked list: each node knows both previous and next nodes

## 6. Sorting and Searching

- **Sorting**
    - Rearranging data in order
        - Efficient sorting requires appropriate data structures
        - Items must have comparable attributes (sort key)
    - Sorting affects search efficiency
    - Ascending and descending order

- **Definition of Sorting**
    - Rearranging records in order of a key
        - Record: object to be sorted
        - Field: attributes of a record
        - Key (sort key): attribute used as sorting criterion

- **Types of Sorting**
    - By location:
        - Internal sorting: all data in main memory
        - External sorting: data mainly on external storage, only part in memory (for large data)
    - By complexity/efficiency:
        - Simple, inefficient: insertion sort, selection sort, bubble sort
        - Complex, efficient: quicksort, heap sort, merge sort, radix sort
    - By stability:
        - Stability: whether records with the same key retain their relative order after sorting
        - Stable: insertion sort, bubble sort, merge sort

- **Basic Sorting Algorithms**
    - **Selection Sort**
        - Selects the smallest number and moves it to the front
        - Divides the list into unsorted and sorted parts
        - In-place sorting (no extra array)
        - Steps:
            1. Select the smallest number from the unsorted list
            2. Move it to the end of the sorted list
            3. Repeat until the unsorted list is empty
        - Time complexity: $$ O(n^2) $$
            - $$ (n-1) + (n-2) + \cdots + 1 = \frac{n(n-1)}{2} = O(n^2) $$

    - **Insertion Sort**
        - Insert a new record into the correct position in the sorted part
        - In-place sorting
        - Steps:
            1. Select the correct position for the new record
            2. Move existing records and insert the new record
            3. Repeat until all records are sorted
        - Time complexity:
            - Best case: $$ O(n) $$
            - Worst case: $$ O(n^2) $$

    - **Bubble Sort**
        - Compare adjacent records and swap if out of order
        - After each pass, the largest record moves to the end
        - In-place sorting
        - Steps:
            1. Perform compare-swap for the entire list
            2. Repeat for the remaining unsorted part
        - Time complexity: $$ O(n^2) $$

- **Sorting Applications**
    - Set operations: sorting can improve time complexity for set comparison, union, difference, intersection

- **Searching**
    - Finding something among data
        - Example: finding a product, searching a website with words/phrases
    - Definition: finding a record with a specific search key in a table
        - Table: set of records
        - Search key: key to identify records
    - Table organization affects search efficiency
    - **Map/Dictionary** (e.g., Python dict): data structure for searching
        - Entry: record with a key
        - Key: search key (e.g., word, name)
        - Value: value associated with the key

- **Searching Algorithms**
    - **Sequential Search**
        - Simple and intuitive
        - Works for unsorted tables: checks each record in order
        - Time complexity: $$ O(n) $$

    - **Binary Search**
        - For sorted tables (e.g., dictionary lookup)
            1. Check the middle value to determine which half to search
            2. Each step halves the number of items to check
        - Not suitable for frequent insertions/deletions
        - Time complexity: $$ O(\log_2 n) $$

    - **Interpolation Search**
        - Variant of binary search for sorted tables
            - Predicts the likely position of the search key
            - Divides the list unevenly based on key value
            - Formula:
                $$
                \text{position} = \text{low} + (\text{high} - \text{low}) \cdot \frac{k - A[\text{low}]}{A[\text{high}] - A[\text{low}]}
                $$
        - Time complexity: $$ O(\log_2 n) $$

- **Advanced Search: Hashing**
    - Uses arithmetic operations on the key to compute the address
        - Hash function: computes storage address from a key
        - Hash address: address calculated by the hash function
        - Hash table: table storing records at hash addresses
    - Time complexity: $$ O(1) $$
    - **Collision**: different keys map to the same address
        - Synonym: keys causing collisions
    - **Overflow**: more collisions than slots
    - **Linear Probing**: checks next slots for empty space
        - Steps:
            1. Repeat linear probing until an empty slot is found
            2. Store record if space exists
            3. Wrap to start if end is reached
            4. If back to collision point, table is full
    - **Clustering**: records cluster at collision points, reducing efficiency
    - **Deletion**: deletion in linear probing can make search impossible
    - **Collision Resolution**:
        - Quadratic probing
        - Double hashing (rehashing): uses a second hash function
        - Chaining: store multiple records in a bucket (linked list)
    - **Good Hash Function**:
        - Few collisions
        - Uniform address distribution
        - Fast calculation
    - **Examples**:
        - Division: $$ h(k) = k \% M $$ (M is prime)
        - Folding: for large keys
        - Mid-square: use middle bits of squared key
        - Bit extraction, digit analysis
    - **Performance**: consider loading factor (density)

## 7. Tree

- **Tree**
    - Data structure suitable for representing hierarchical data
        - Examples: organization chart, family tree, computer folder structure
    - Applications:
        - Search tree (search)
        - Heap tree (priority queue)
        - Decision tree (decision structure)
    - Trees are defined recursively (hence recursive algorithms are common)

- **Tree Terminology**

| Term | Meaning |
|------|---------|
| Root node | The highest node in a hierarchical structure; every node is the root of its own subtree |
| Edge | Connection between nodes |
| Parent node, Child node | Nodes directly connected by an edge; parent is above, child is below |
| Sibling node | Nodes sharing the same parent |
| Ancestor node, Descendant node | Nodes on the path from a node to the root; all nodes below a node |
| Terminal (leaf) node | Node with no children (opposite: non-terminal node) |
| Degree of node | Number of children a node has |
| Degree of tree | Largest node degree in the tree |
| Level | Number assigned to each layer (root is level 1, increases downward) |
| Height of tree | Maximum level in the tree |
| Forest | Set of trees |

- **General Tree Representation**
    - General tree: nodes can have any number of children
    - Typically represented with linked structures
        - Data field: node value, links: child nodes
        - Number of links varies per node, often managed as a list
    - Simplified: two links per node (child, sibling)

- **Binary Tree**
    - Each node has up to two subtrees
        - Defined recursively
        - Subtrees can be empty
        - Children are ordered (left, right)
    - Definition:
        1. Empty, or
        2. A root and left/right subtrees (which are themselves binary trees)

- **Types of Binary Trees**
    - **Full Binary Tree**: every level is completely filled
        - Numbering: root is 1, then left to right
    - **Complete Binary Tree**: all levels except possibly the last are full; last level filled left to right

- **Binary Tree Properties**
    - If there are $$ n $$ nodes, there are $$ n - 1 $$ edges
    - If height is $$ k $$, has up to $$ 2^k - 1 $$ nodes
    - Height of a binary tree with $$ n $$ nodes: $$ \log_2 n + 1 $$ to $$ n $$
        - $$ n \leq 2^k - 1 \Rightarrow \log_2 n + 1 \leq k $$

- **Binary Tree Representation**
    - **Array Representation**
        - Steps:
            1. Compute the height and allocate an array of size $$ 2^k - 1 $$
            2. Use indices as node numbers
        - Suitable for full or complete binary trees
        - Memory waste for skewed trees
        - Simple but limited by array size and tree height
    - **Linked Representation**
        - Each node has two links (left, right child)

- **Binary Tree Traversal**
    - Visit every node in the tree exactly once
        - Preorder (VLR): root → left → right (e.g., level calculation, structured document output)
        - Inorder (LVR): left → root → right (e.g., sorting)
        - Postorder (LRV): left → right → root (e.g., folder size calculation)
    - Level-order traversal: visit nodes by level using a queue (not recursive)

- **Binary Tree Applications**
    - Morse code decision tree
        - Encoding: alphabet → Morse code, $$ O(1) $$
        - Decoding: Morse code → alphabet, $$ O(n) $$
        - Decision tree-based decoding: $$ O(\log_2 n) $$

- **Heap Tree**
    - Heap operations (insert, delete)
    - Heap implementation
    - Max heap
    - Heap as a priority queue

- **Huffman Coding Tree**
    - Huffman code generation using a min-heap

## 8. Search Tree

- **Search Tree**
- **Binary Search Tree**
    - Operations: search, insert, delete
    - Performance
    - Map based on binary search tree
- **Balanced Binary Search Tree**
    - Operations (insert, etc.)
    - Map using balanced binary search tree

## 9. Graph

- **Graph**
- Definition of graph
- Types of graphs
- Graph terminology
- Graph representation
- Graph traversal
    - Depth-First Search (DFS, adjacency list)
    - Breadth-First Search (BFS, adjacency list)
- Connected component check
- Spanning tree
- Topological sort

## 10. Weighted Graph

- **Weighted Graph**
- Weighted graph representation
    - Using adjacency matrix
    - Using adjacency list
- Minimum spanning tree
    - Kruskal's algorithm
    - Prim's algorithm
- Shortest path
    - Dijkstra's algorithm
    - Floyd-Warshall algorithm

### Note on Formulas

- **Selection Sort**: $$ O(n^2) $$ is correct.
- **Insertion Sort**: Best $$ O(n) $$, worst $$ O(n^2) $$ is correct.
- **Bubble Sort**: $$ O(n^2) $$ is correct.
- **Binary Search**: $$ O(\log_2 n) $$ is correct.
- **Interpolation Search**: $$ O(\log_2 \log_2 n) $$ is correct.
- **Hashing**: $$ O(1) $$ average case is correct, but can degrade with collisions.
- **Binary Tree Properties**: $$ n \leq 2^k - 1 \Rightarrow \log_2 n + 1 \leq k $$ is correct.
