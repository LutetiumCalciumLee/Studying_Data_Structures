<details>
<summary>ENG (English Version)</summary>

# Data Structures

## Chapter 1: Data Structures and Algorithms

### Data Structure
- **Definition**: Various ways to organize and structure data in a computer.
- **Purpose**: Each data type has efficient organizing rules.
- **Types**: Simple (numbers, characters) and compound (containers for multiple data items).
- **Categories**: Linear and non-linear data structures.

### Algorithm
- **Definition**: A procedure, method, or set of instructions to solve a problem.
- **Formula**: Program = Data Structure + Algorithm.
- **Properties**:
  - **Input**: Zero or more inputs.
  - **Output**: At least one output.
  - **Definiteness**: Instructions must be clear and unambiguous.
  - **Finiteness**: Must terminate after a finite number of steps.
  - **Effectiveness**: Instructions must be executable.
- **Description Methods**: Natural language, flowchart, pseudocode, programming language.

### Abstract Data Type (ADT)
- **Definition**: A data type defined abstractly.
- **Characteristics**: Defines only data and operations, not the implementation method, focusing on core structure and behavior.
- **Interface**: Exposes only the interface (information hiding).
- **Implementation**: Best implemented as a class.

### Algorithm Performance
- **Factors**: Calculation speed, memory usage, functionality achievement. Speed is often prioritized.
- **Measurement Challenges**: Requires implementation, consistent hardware/software environments, and is data-dependent.

### Complexity Analysis
- **Purpose**: Analyze algorithm efficiency without actual implementation.
- **Focus**: How execution time changes as input size n increases.
- **Method**: Hardware and software environment-independent evaluation.
- **Time Complexity Function**: T(n) - the number of operations as a function of n.
- **Big O Notation**: Considers only the highest order term as n increases.
- **Big Omega (Ω)**: Indicates the lower bound of a function.
- **Big Theta (Θ)**: Indicates both upper and lower bounds with the same function.

### Input Data
- **Execution Time Variation**: Depends on the input data.
- **Cases**: Best case, average case, and worst case.
- **Importance**: Worst-case time is critical for systems like aircraft control, games, and robotics.

## Chapter 2: List & Set

### List / Linear List
- **Definition**: A linear data structure with items arranged in order.
- **Characteristics**: Items have order/position; insertion and addition are possible at any position.
- **List vs. Set**: The presence of order among items.

### List Implementation Methods
- **Array Structure**:
  - Items are in contiguous memory, allowing O(1) access.
  - Inefficient for insertions/deletions in the middle and difficult to resize.
- **Linked Structure**:
  - Items are linked, allowing O(1) insertion/deletion.
  - Access time is O(n) as it requires traversal.

### List Applications
- **Line Editor**: Functions like insert, delete, replace, print, load, save, and quit.

### Set
- **Definition**: A collection that does not allow duplicate elements.
- **Characteristics**: No duplicates, no order among elements.
- **Implementation**: Operations include union, intersect, difference, contains, insert, delete.

## Chapter 3: Stack

### Stack Definition
- **Structure**: Last-In First-Out (LIFO) data structure.
- **Operations**: Insertion (push) and deletion (pop) only occur at the top.
- **Simplicity**: More restricted I/O makes operations simpler than lists.

### Stack Applications
- Editor "undo" functions, browser "back" button, system stack for function calls, parenthesis checking, calculators, and maze solving.

### Stack Implementation
- **Python-based Stack ADT**: Operations include `push`, `pop`, `peek`, `isEmpty`, `size`, `clear`. Using the rear of a list is O(1); using the front is O(n).

### Stack Applications
- **Parentheses Checking**: Validate matching parentheses.
- **Expression Evaluation**: Convert infix to postfix notation.
- **Maze Solving**: Depth-first search (DFS).

## Chapter 4: Queue & Deque

### Queue
- **Structure**: First-In First-Out (FIFO) data structure.
- **Operations**: Insertion (enqueue) at the rear, deletion (dequeue) at the front.

### Queue Applications
- Buffers, call queues, print job queues, real-time video streaming, and simulations (e.g., bank tickets, airport runways).

### Queue Implementation
- **Linear Queue**: Simple implementation with lists, but can be inefficient.
- **Circular Queue**:
  - Manages `front` and `rear` pointers in a fixed-size array.
  - Empty state: front == rear
  - Full state: front % M == (rear + 1) % M
  - Distinguishes empty/full states by keeping one space unused.

### Deque (Double-ended Queue)
- **Structure**: Allows insertion and deletion at both ends.
- **Flexibility**: More flexible than a stack or queue, but cannot access the middle.

### Priority Queue
- **Definition**: A queue where each item has a priority.
- **Behavior**: Higher priority data is processed first. Can be configured to act as a standard queue (FIFO) or stack (LIFO).
- **Applications**: Simulations, network traffic control, OS task scheduling, and algorithms like Huffman coding, Kruskal's, Dijkstra's, and A*.

## Chapter 5: Linked Structures

### Linked Structure
- **Definition**: A method of managing scattered data by connecting nodes with links.
- **Linked List**: A linear arrangement of linked nodes.

### Linked vs. Array Structure
- **Capacity**: Dynamic (linked) vs. Fixed (array).
- **Insertion/Deletion**: O(1) (linked) vs. O(n) (array).
- **Access**: O(n) (linked) vs. O(1) (array).

### Basic Linked List Structure
- **Node**: Contains a data field and a link field (pointer to the next node).
- **Head Pointer**: Stores the address of the first node.

### Types of Linked Lists
- **Singly Linked List**: Connected in one direction.
- **Circular Linked List**: The last node points to the first.
- **Doubly Linked List**: Each node points to both the previous and next nodes.

### Linked List Applications
- **Linked Stack/Queue/Deque**: Implementations of these data structures using nodes.

## Chapter 6: Sorting and Searching

### Sorting
- **Definition**: Rearranging data in a specific order (ascending or descending).
- **Impact**: Affects search efficiency.

### Sorting Classification
- **By Location**: Internal (in memory) vs. External (on disk).
- **By Efficiency**:
  - Simple (O(n²)): Selection sort, Insertion sort, Bubble sort.
  - Complex (O(n log n)): Quicksort, Heap sort, Merge sort.
- **By Stability**: Whether the relative order of equal keys is preserved.

### Simple Sorting Algorithms
- **Selection Sort**: Repeatedly select the smallest item and move it to the front. O(n²).
- **Insertion Sort**: Insert each item into its correct position in the sorted part of the array. O(n) best, O(n²) worst.
- **Bubble Sort**: Repeatedly swap adjacent items if they are in the wrong order. O(n²).

### Searching
- **Definition**: Finding a record with a desired search key.
- **Map/Dictionary**: A data structure optimized for searching with key-value pairs.

### Simple Search Algorithms
- **Sequential Search**: Check each item from the beginning. O(n). Works on unsorted data.
- **Binary Search**: Repeatedly check the middle item to halve the search space. O(log₂n). Requires sorted data.
- **Interpolation Search**: A variant of binary search that predicts the key's position. O(log₂(log₂n)) on average.

### Advanced Search: Hashing
- **Definition**: Uses a hash function to compute a storage address directly from a key.
- **Complexity**: O(1) in the ideal case.
- **Collision**: Occurs when different keys map to the same address.
- **Collision Resolution**: Linear probing, quadratic probing, double hashing, chaining.

### Hash Function Examples
- **Division method**: h(k) = k % M (M is prime)
- Other methods: Folding, mid-square, bit extraction, digit analysis, string hashing

### Map Applications
- Dictionaries, symbol tables. Can be implemented with lists (sequential search) or hash tables (hashing).

## Chapter 7: Tree

### Tree
- **Definition**: A data structure for representing hierarchical data.
- **Examples**: Org charts, family trees, file systems.
- **Applications**: Search trees, heaps, decision trees.

### Binary Tree
- **Definition**: A tree where each node has at most two children (left and right).
- **Types**: Full (all levels filled), Complete (last level filled left-to-right).
- **Properties**: 
  - A tree with n nodes has n-1 edges
  - Height k tree has at most 2^k - 1 nodes
  - Height is between ceiling(log₂(n+1)) and n

### Binary Tree Representation
- **Array**: Good for complete trees, size 2^k - 1, wasteful for skewed trees.
- **Linked**: Flexible, with nodes containing data and left/right child pointers.

### Binary Tree Traversal
- **Preorder (VLR)**: Visit root, traverse left, traverse right.
- **Inorder (LVR)**: Traverse left, visit root, traverse right.
- **Postorder (LRV)**: Traverse left, traverse right, visit root.
- **Level-order**: Visit nodes level by level using a queue.

### Binary Tree Operations
- **Node counting**: Count all nodes recursively
- **Leaf counting**: Count nodes with no children
- **Height calculation**: Find maximum depth

### Heap
- **Definition**: A complete binary tree used to quickly find the max (max heap) or min (min heap) element.
- **Properties**:
  - Max heap: parent key >= child key
  - Min heap: parent key <= child key
- **Operations**: Insertion and deletion are O(log₂n).
- **Representation**: Array is most efficient
- **Applications**: Priority queue implementation.

### Huffman Coding Tree
- **Purpose**: Creates variable-length codes based on character frequency for data compression.
- **Construction**: Use min heap to build tree from bottom up
- **Efficiency**: More efficient than fixed-length codes

## Chapter 8: Search Tree

### Binary Search Tree (BST)
- **Definition**: A binary tree for efficient searching, insertion, and deletion. Average time complexity is O(log₂n).
- **Properties**: 
  - All nodes have unique keys
  - Left subtree keys < root key < right subtree keys
  - Both subtrees are also BSTs
- **Performance**: Highly dependent on tree shape. A skewed tree degrades to O(n).

### BST Operations
- **Search by Key**: O(log₂n) average case
- **Search by Value**: O(n) - must check all nodes
- **Min/Max Search**: Follow leftmost/rightmost path
- **Insert**: O(log₂n) - follow search path, insert at failure point
- **Delete**: Most complex with 3 cases:
  - Case 1: Leaf node - simply remove
  - Case 2: One child - connect child to parent
  - Case 3: Two children - replace with successor

### AVL Tree
- **Purpose**: A self-balancing BST that guarantees O(log₂n) performance.
- **Balance Factor**: Height difference between left and right subtrees
- **Constraint**: Balance factor must be -1, 0, or 1
- **Rebalancing**: Use rotations when balance factor becomes ±2
- **Rotation Types**:
  - Single rotation: LL, RR
  - Double rotation: LR, RL

## Chapter 9: Graph

### Graph
- **Definition**: A data structure representing relationships between connected objects (vertices/nodes) via edges.
- **Notation**: G = (V, E)
  - V(G): set of vertices
  - E(G): set of edges
- **Types**: Undirected, directed, weighted.
- **Applications**: Maps, social networks, computer networks.

### Graph Terminology
- **Adjacent Vertex**: Vertices directly connected by edge
- **Degree**: Number of edges connected to vertex
- **Path**: Sequence of vertices connected by edges
- **Simple Path**: Path with no repeated edges
- **Cycle**: Path where start and end vertices are same
- **Connected Graph**: Graph where path exists between all vertex pairs
- **Complete Graph**: Graph with edges between all vertex pairs

### Graph Representation
- **Adjacency Matrix**: n×n matrix. O(1) edge lookup, but O(n²) space. Good for dense graphs.
- **Adjacency List**: A list of adjacent vertices for each vertex. O(n+e) space. Good for sparse graphs.

### Graph Traversal
- **Depth-First Search (DFS)**: Explores as far as possible along each branch before backtracking. Uses a stack.
- **Breadth-First Search (BFS)**: Explores all neighbor nodes at the present depth before moving on. Uses a queue.

### Graph Applications
- **Connected Component Detection**: Find separate connected parts
- **Spanning Tree**: Tree connecting all vertices with n-1 edges
- **Topological Sort**: Order vertices respecting dependencies (DAG only)

## Chapter 10: Weighted Graph

### Weighted Graph
- **Definition**: A graph where each edge has an associated weight or cost.
- **Representation**: G = (V, E, w)
- **Path Length**: Sum of weights along path

### Minimum Spanning Tree (MST)
- **Definition**: A spanning tree with the minimum possible total edge weight.
- **Properties**: n-1 edges, no cycles, connects all vertices
- **Applications**: Communication networks, road networks, circuit design

### MST Algorithms
- **Kruskal's Algorithm**:
  - Strategy: Sort edges by weight, add if no cycle created
  - Time Complexity: O(e log e)
  - Uses Union-Find for cycle detection
  - Better for sparse graphs
- **Prim's Algorithm**:
  - Strategy: Start with vertex, expand tree by adding minimum weight edge
  - Time Complexity: O(n²)
  - Better for dense graphs

### Shortest Path
- **Definition**: Path with minimum total weight between vertices
- **Applications**: Navigation, network routing, resource optimization

### Shortest Path Algorithms
- **Dijkstra's Algorithm**:
  - Purpose: Single-source shortest path to all vertices
  - Strategy: Greedy approach, always select minimum distance vertex
  - Time Complexity: O(n²)
  - Constraint: Non-negative edge weights
  - Maintains dist array and found set
- **Floyd-Warshall Algorithm**:
  - Purpose: All-pairs shortest path
  - Strategy: Dynamic programming with intermediate vertices
  - Time Complexity: O(n³)
  - Formula: A^k[i][j] = min(A^(k-1)[i][j], A^(k-1)[i][k] + A^(k-1)[k][j])
  - Handles negative weights (but not negative cycles)

### Algorithm Comparison
- **Kruskal vs Prim**: Kruskal better for sparse graphs, Prim for dense graphs
- **Dijkstra vs Floyd-Warshall**: Dijkstra for single source, Floyd-Warshall for all pairs

</details>

<details>
<summary>KOR (한국어 버전)</summary>

# 자료구조

## 1장: 자료구조와 알고리즘

### 자료구조
- **정의**: 컴퓨터에서 데이터를 조직하고 구조화하는 다양한 방법.
- **목적**: 각 데이터 유형에 맞는 효율적인 정리 규칙을 제공.
- **종류**: 단순 자료구조(숫자, 문자)와 복합 자료구조(여러 데이터를 함께 저장하는 컨테이너).
- **분류**: 선형 자료구조와 비선형 자료구조.

### 알고리즘
- **정의**: 문제를 해결하기 위한 절차, 방법, 명령어의 집합.
- **공식**: 프로그램 = 자료구조 + 알고리즘.
- **특성**:
  - **입력**: 0개 이상의 입력.
  - **출력**: 1개 이상의 출력.
  - **명확성**: 명령어는 명확하고 모호하지 않아야 함.
  - **유한성**: 유한한 단계 후에 반드시 종료해야 함.
  - **유효성**: 명령어는 실행 가능해야 함.
- **기술 방법**: 자연어, 순서도, 의사코드, 프로그래밍 언어.

### 추상 데이터 타입 (ADT)
- **정의**: 추상적으로 정의된 데이터 타입.
- **특징**: 데이터와 연산만 정의하고 구현 방법은 명시하지 않아 핵심 구조와 동작에 집중.
- **인터페이스**: 인터페이스만 노출 (정보 은닉).
- **구현**: 클래스로 구현하는 것이 가장 적합.

### 알고리즘 성능
- **요인**: 계산 속도, 메모리 사용량, 기능 달성 여부. 속도가 주로 우선시됨.
- **측정의 어려움**: 구현이 필요하고, 동일한 하드웨어/소프트웨어 조건이 요구되며, 데이터에 따라 변동.

### 복잡도 분석
- **목적**: 실제 구현 없이 알고리즘 효율성을 분석.
- **초점**: 입력 크기 n이 증가할 때 실행 시간이 어떻게 증가하는지 분석.
- **방법**: 하드웨어와 소프트웨어 환경에 독립적인 평가.
- **시간 복잡도 함수**: T(n) - n의 함수로서의 연산 횟수.
- **빅오 표기법**: n이 증가할 때 최고 차수 항만 고려.
- **빅오메가 (Ω)**: 함수의 하한을 나타냄.
- **빅세타 (Θ)**: 동일한 함수로 상한과 하한을 모두 나타냄.

### 입력 데이터
- **실행 시간 변화**: 입력 데이터에 따라 달라짐.
- **경우**: 최선의 경우, 평균의 경우, 최악의 경우.
- **중요성**: 항공기 제어, 게임, 로봇공학 등 중요한 시스템에서는 최악의 실행 시간이 중요.

## 2장: 리스트 & 집합

### 리스트 / 선형 리스트
- **정의**: 항목들이 순서대로 배열된 선형 자료구조.
- **특징**: 항목에 순서/위치가 있고, 임의의 위치에 삽입 및 추가 가능.
- **리스트 vs 집합**: 항목 간 순서 유무의 차이.

### 리스트 구현 방법
- **배열 구조**:
  - 인접한 메모리에 항목을 저장하여 O(1) 접근이 가능.
  - 중간 연산이 비효율적이고 용량 변경이 어려움.
- **연결 구조**:
  - 링크를 사용하여 항목을 연결하므로 O(1) 삽입/삭제가 가능.
  - 접근 시간은 탐색이 필요하여 O(n)임.

### 리스트 응용
- **라인 에디터**: 삽입, 삭제, 교체, 출력, 파일 로드, 저장, 종료 기능 구현.

### 집합 (Set)
- **정의**: 중복된 요소를 허용하지 않는 컬렉션.
- **특징**: 중복 요소 없음, 요소 간 순서 없음.
- **구현**: 합집합, 교집합, 차집합, 포함 여부, 삽입, 삭제 등의 연산 구현.

## 3장: 스택

### 스택 정의
- **구조**: 후입선출(LIFO) 자료구조.
- **연산**: 맨 위(top)에서만 삽입(push)과 삭제(pop)가 일어남.
- **단순성**: 입출력이 제한되어 리스트보다 연산이 간단.

### 스택 응용
- 문서 편집기 "실행 취소", 웹 브라우저 "뒤로 가기", 함수 호출을 위한 시스템 스택, 괄호 검사, 계산기, 미로 찾기.

### 스택 구현
- **Python 기반 스택 ADT**: push, pop, peek, isEmpty, size, clear 연산. 리스트의 맨 뒤를 사용하면 O(1), 맨 앞을 사용하면 O(n).

### 스택 응용
- **괄호 검사**: 코드의 괄호 쌍이 맞는지 검증.
- **수식 계산**: 중위 표기법을 후위 표기법으로 변환.
- **미로 탐색**: 깊이 우선 탐색(DFS).

## 4장: 큐 & 덱

### 큐
- **구조**: 선입선출(FIFO) 자료구조.
- **연산**: 뒤(rear)에서 삽입, 앞(front)에서 삭제.

### 큐 응용
- 버퍼, 통화 대기열, 인쇄 작업 큐, 실시간 비디오 스트리밍, 시뮬레이션(은행 대기표, 공항 활주로).

### 큐 구현
- **선형 큐**: 리스트를 사용한 간단한 구현.
- **원형 큐**:
  - 고정 크기 배열에서 front와 rear 포인터를 관리.
  - 공백 상태: front == rear
  - 포화 상태: front % M == (rear + 1) % M
  - 공백/포화 상태 구분을 위해 항상 한 칸을 비워 둠.

### 덱 (Double-ended Queue)
- **구조**: 양쪽 끝에서 삽입과 삭제가 모두 가능한 큐.
- **유연성**: 스택이나 큐보다 입출력이 유연하지만, 중간 삽입/삭제는 불가.

### 우선순위 큐
- **정의**: 각 항목에 우선순위 개념이 있는 큐.
- **동작**: 우선순위가 높은 데이터가 먼저 처리됨. 우선순위 부여 방식에 따라 큐(FIFO)나 스택(LIFO)처럼 동작 가능.
- **응용**: 시뮬레이션, 네트워크 트래픽 제어, OS 작업 스케줄링, 허프만 코딩, 크루스칼/다익스트라/A* 알고리즘.

## 5장: 연결 구조

### 연결 구조
- **정의**: 흩어진 데이터를 링크로 연결하여 관리하는 방식.
- **연결 리스트**: 연결 구조를 선형으로 배열한 것.

### 연결 구조 vs 배열 구조
- **용량**: 동적 (연결) vs 고정 (배열).
- **삽입/삭제**: O(1) (연결) vs O(n) (배열).
- **접근**: O(n) (연결) vs O(1) (배열).

### 기본 연결 리스트 구조
- **노드**: 데이터 필드와 다음 노드를 가리키는 링크 필드로 구성.
- **헤드 포인터**: 첫 번째 노드의 주소를 저장.

### 연결 리스트 종류
- **단순 연결 리스트**: 한 방향으로 연결.
- **원형 연결 리스트**: 마지막 노드가 첫 노드를 가리킴.
- **이중 연결 리스트**: 각 노드가 이전 및 다음 노드를 모두 가리킴.

### 연결 리스트 응용
- **연결 스택/큐/덱**: 노드를 사용하여 각 자료구조를 구현.

## 6장: 정렬과 탐색

### 정렬
- **정의**: 데이터를 특정 순서(오름차순, 내림차순)로 재배열하는 것.
- **영향**: 탐색 효율성에 영향을 줌.

### 정렬 분류
- **위치 기준**: 내부 정렬(메모리 내) vs 외부 정렬(디스크 사용).
- **효율성 기준**:
  - 단순(O(n²)): 선택, 삽입, 버블 정렬.
  - 복잡(O(n log n)): 퀵, 힙, 병합 정렬.
- **안정성 기준**: 같은 키 값의 상대적 순서 유지 여부.

### 단순 정렬 알고리즘
- **선택 정렬**: 가장 작은 항목을 찾아 맨 앞으로 이동. O(n²).
- **삽입 정렬**: 각 항목을 정렬된 부분의 올바른 위치에 삽입. 최선 O(n), 최악 O(n²).
- **버블 정렬**: 인접 항목을 비교하여 순서가 맞지 않으면 교환. O(n²).

### 탐색
- **정의**: 원하는 탐색 키를 가진 레코드를 찾는 것.
- **맵/사전**: 키-값 쌍으로 탐색에 최적화된 자료구조.

### 단순 탐색 알고리즘
- **순차 탐색**: 처음부터 순서대로 확인. O(n). 정렬 불필요.
- **이진 탐색**: 중간 항목을 확인하여 탐색 공간을 절반으로 줄임. O(log₂n). 정렬 필요.
- **보간 탐색**: 키의 예상 위치를 예측하는 이진 탐색의 변형. 평균 O(log₂(log₂n)).

### 고급 탐색: 해싱
- **정의**: 해시 함수를 사용해 키로부터 저장 주소를 직접 계산.
- **복잡도**: 이상적인 경우 O(1).
- **충돌**: 다른 키가 같은 주소에 매핑되는 현상.
- **충돌 해결**: 선형 조사법, 이차 조사법, 이중 해싱, 체이닝.

### 해시 함수 예시
- **나눗셈법**: h(k) = k % M (M은 소수)
- 기타: 폴딩법, 중간제곱법, 비트추출법, 숫자분석법, 문자열 해싱

### 맵 응용
- 사전, 심볼 테이블 등. 리스트(순차 탐색) 또는 해시 테이블로 구현 가능.

## 7장: 트리

### 트리
- **정의**: 계층적 데이터를 표현하기에 적합한 자료구조.
- **예시**: 조직도, 가계도, 파일 시스템.
- **응용**: 탐색 트리, 힙, 결정 트리.

### 이진 트리
- **정의**: 각 노드가 최대 두 개의 자식(왼쪽, 오른쪽)을 갖는 트리.
- **종류**: 포화 이진 트리(모든 레벨 꽉 참), 완전 이진 트리(마지막 레벨은 왼쪽부터 채움).
- **속성**: 
  - 노드 n개일 때, 간선은 n-1개
  - 높이 k 트리는 최대 2^k - 1개 노드
  - 높이는 ceiling(log₂(n+1))에서 n 사이

### 이진 트리 표현
- **배열**: 완전 이진 트리에 적합하나 크기 2^k - 1, 편향 트리에선 공간 낭비 심함.
- **연결**: 유연하지만, 노드들이 데이터와 왼쪽/오른쪽 자식 포인터를 가짐.

### 이진 트리 순회
- **전위 순회 (VLR)**: 루트 방문 → 왼쪽 순회 → 오른쪽 순회.
- **중위 순회 (LVR)**: 왼쪽 순회 → 루트 방문 → 오른쪽 순회.
- **후위 순회 (LRV)**: 왼쪽 순회 → 오른쪽 순회 → 루트 방문.
- **레벨 순회**: 큐를 사용하여 레벨 순으로 노드 방문.

### 이진 트리 연산
- **노드 개수 세기**: 재귀적으로 모든 노드 계산
- **리프 개수 세기**: 자식이 없는 노드 계산
- **높이 계산**: 최대 깊이 찾기

### 힙
- **정의**: 최댓값(최대 힙) 또는 최솟값(최소 힙)을 빠르게 찾기 위한 완전 이진 트리.
- **속성**:
  - 최대 힙: 부모 키 >= 자식 키
  - 최소 힙: 부모 키 <= 자식 키
- **연산**: 삽입과 삭제는 O(log₂n).
- **표현**: 배열이 가장 효율적
- **응용**: 우선순위 큐 구현.

### 허프만 코딩 트리
- **목적**: 데이터 압축을 위해 문자 빈도에 따라 가변 길이 코드를 생성.
- **구축**: 최소 힙을 사용하여 아래에서 위로 트리 구축
- **효율성**: 고정 길이 코드보다 효율적

## 8장: 탐색 트리

### 이진 탐색 트리 (BST)
- **정의**: 효율적인 탐색, 삽입, 삭제를 위한 이진 트리. 평균 시간 복잡도는 O(log₂n).
- **속성**: 
  - 모든 노드는 유일한 키를 가짐
  - 왼쪽 서브트리 키 < 루트 키 < 오른쪽 서브트리 키
  - 양쪽 서브트리 모두 BST
- **성능**: 트리 모양에 따라 크게 달라짐. 편향된 경우 O(n)으로 저하.

### BST 연산
- **키로 탐색**: 평균 O(log₂n)
- **값으로 탐색**: O(n) - 모든 노드 확인 필요
- **최소/최대 탐색**: 가장 왼쪽/오른쪽 경로 따라감
- **삽입**: O(log₂n) - 탐색 경로를 따라가서 실패 지점에 삽입
- **삭제**: 3가지 경우로 가장 복잡:
  - 경우 1: 리프 노드 - 단순 제거
  - 경우 2: 한 개의 자식 - 자식을 부모에 연결
  - 경우 3: 두 개의 자식 - 후계자로 교체

### AVL 트리
- **목적**: O(log₂n) 성능을 보장하는 자가 균형 이진 탐색 트리.
- **균형 인수**: 왼쪽과 오른쪽 서브트리의 높이 차이
- **제약**: 균형 인수는 -1, 0, 1 중 하나여야 함
- **재균형**: 균형 인수가 ±2가 되면 회전 사용
- **회전 종류**:
  - 단일 회전: LL, RR
  - 이중 회전: LR, RL

## 9장: 그래프

### 그래프
- **정의**: 연결된 객체(정점/노드)들 간의 관계를 간선으로 표현하는 자료구조.
- **표기**: G = (V, E)
  - V(G): 정점의 집합
  - E(G): 간선의 집합
- **종류**: 무방향, 방향, 가중치 그래프.
- **응용**: 지도, 소셜 네트워크, 컴퓨터 네트워크.

### 그래프 용어
- **인접 정점**: 간선으로 직접 연결된 정점
- **차수**: 정점에 연결된 간선의 수
- **경로**: 간선으로 연결된 정점의 시퀀스
- **단순 경로**: 반복된 간선이 없는 경로
- **사이클**: 시작과 끝 정점이 같은 경로
- **연결 그래프**: 모든 정점 쌍 사이에 경로가 존재하는 그래프
- **완전 그래프**: 모든 정점 쌍 사이에 간선이 있는 그래프

### 그래프 표현
- **인접 행렬**: n×n 행렬. O(1) 간선 조회, O(n²) 공간. 밀집 그래프에 적합.
- **인접 리스트**: 각 정점의 인접 정점 리스트. O(n+e) 공간. 희소 그래프에 적합.

### 그래프 탐색
- **깊이 우선 탐색 (DFS)**: 한 경로를 끝까지 탐색 후 돌아옴. 스택 사용.
- **너비 우선 탐색 (BFS)**: 현재 깊이의 모든 이웃을 탐색 후 다음 깊이로 이동. 큐 사용.

### 그래프 응용
- **연결 요소 탐지**: 분리된 연결 부분 찾기
- **신장 트리**: n-1개 간선으로 모든 정점 연결
- **위상 정렬**: 의존성을 고려한 정점 순서 (방향 비순환 그래프에만 적용)

## 10장: 가중치 그래프

### 가중치 그래프
- **정의**: 각 간선에 가중치나 비용이 할당된 그래프.
- **표현**: G = (V, E, w)
- **경로 길이**: 경로를 따라가는 가중치의 합

### 최소 신장 트리 (MST)
- **정의**: 가능한 총 간선 가중치가 최소인 신장 트리.
- **속성**: n-1개 간선, 사이클 없음, 모든 정점 연결
- **응용**: 통신 네트워크, 도로 네트워크, 회로 설계

### MST 알고리즘
- **크루스칼 알고리즘**:
  - 전략: 간선을 가중치 순으로 정렬, 사이클을 형성하지 않으면 추가
  - 시간 복잡도: O(e log e)
  - Union-Find로 사이클 탐지
  - 희소 그래프에 적합
- **프림 알고리즘**:
  - 전략: 한 정점에서 시작하여 최소 가중치 간선을 추가하며 트리 확장
  - 시간 복잡도: O(n²)
  - 밀집 그래프에 적합

### 최단 경로
- **정의**: 두 정점 사이의 총 가중치가 최소인 경로
- **응용**: 내비게이션, 네트워크 라우팅, 자원 최적화

### 최단 경로 알고리즘
- **다익스트라 알고리즘**:
  - 목적: 단일 출발점에서 다른 모든 정점까지의 최단 경로
  - 전략: 탐욕 방식, 항상 최소 거리 정점 선택
  - 시간 복잡도: O(n²)
  - 제약: 음수 간선 가중치 불가
  - dist 배열과 found 집합 유지
- **플로이드-워셜 알고리즘**:
  - 목적: 모든 정점 쌍 간의 최단 경로
  - 전략: 중간 정점을 이용한 동적 프로그래밍
  - 시간 복잡도: O(n³)
  - 공식: A^k[i][j] = min(A^(k-1)[i][j], A^(k-1)[i][k] + A^(k-1)[k][j])
  - 음수 가중치 처리 가능 (음수 사이클 제외)

### 알고리즘 비교
- **크루스칼 vs 프림**: 희소 그래프는 크루스칼, 밀집 그래프는 프림이 유리
- **다익스트라 vs 플로이드-워셜**: 단일 출발점은 다익스트라, 모든 쌍은 플로이드-워셜

</details>
