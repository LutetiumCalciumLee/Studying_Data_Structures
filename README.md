<details>
<summary>ENG (English Version)</summary>

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
  - Height k tree has at most $$2^k - 1$$ nodes
  - Height is between ceiling($$\log_2(n+1)$$) and n

### Binary Tree Representation
- **Array**: Good for complete trees, size $$2^k - 1$$, wasteful for skewed trees.
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
  - Max heap: parent key ≥ child key
  - Min heap: parent key ≤ child key
- **Operations**: Insertion and deletion are $$O(\log_2 n)$$.
- **Representation**: Array is most efficient
- **Applications**: Priority queue implementation.

### Huffman Coding Tree
- **Purpose**: Creates variable-length codes based on character frequency for data compression.
- **Construction**: Use min heap to build tree from bottom up
- **Efficiency**: More efficient than fixed-length codes

</details>

<details>
<summary>KOR (한국어 버전)</summary>

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
  - 높이 k 트리는 최대 $$2^k - 1$$개 노드
  - 높이는 ceiling($$\log_2 (n+1)$$)에서 n 사이

### 이진 트리 표현
- **배열**: 완전 이진 트리에 적합하나 크기 $$2^k - 1$$, 편향 트리에선 공간 낭비 심함.
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
  - 최대 힙: 부모 키 ≥ 자식 키
  - 최소 힙: 부모 키 ≤ 자식 키
- **연산**: 삽입과 삭제는 $$O(\log_2 n)$$.
- **표현**: 배열이 가장 효율적
- **응용**: 우선순위 큐 구현.

### 허프만 코딩 트리
- **목적**: 데이터 압축을 위해 문자 빈도에 따라 가변 길이 코드를 생성.
- **구축**: 최소 힙을 사용하여 아래에서 위로 트리 구축
- **효율성**: 고정 길이 코드보다 효율적

</details>
