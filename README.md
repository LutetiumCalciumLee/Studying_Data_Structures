<details>
<summary>ENG (English Version)</summary>

## Chapter 8: Search Tree

### Binary Search Tree (BST)
- **Definition**: A binary tree for efficient searching, insertion, and deletion. Average time complexity is $$O(\log_2 n)$$.
- **Properties**: 
  - All nodes have unique keys
  - Left subtree keys < root key < right subtree keys
  - Both subtrees are also BSTs
- **Performance**: Highly dependent on tree shape. A skewed tree degrades to $$O(n)$$.

### BST Operations
- **Search by Key**: $$O(\log_2 n)$$ average case
- **Search by Value**: $$O(n)$$ - must check all nodes
- **Min/Max Search**: Follow leftmost/rightmost path
- **Insert**: $$O(\log_2 n)$$ - follow search path, insert at failure point
- **Delete**: Most complex with 3 cases:
  - Case 1: Leaf node - simply remove
  - Case 2: One child - connect child to parent
  - Case 3: Two children - replace with successor

### AVL Tree
- **Purpose**: A self-balancing BST that guarantees $$O(\log_2 n)$$ performance.
- **Balance Factor**: Height difference between left and right subtrees
- **Constraint**: Balance factor must be -1, 0, or 1
- **Rebalancing**: Use rotations when balance factor becomes ±2
- **Rotation Types**:
  - Single rotation: LL, RR
  - Double rotation: LR, RL

</details>

<details>
<summary>KOR (한국어 버전)</summary>

## 8장: 탐색 트리

### 이진 탐색 트리 (BST)
- **정의**: 효율적인 탐색, 삽입, 삭제를 위한 이진 트리. 평균 시간 복잡도는 $$O(\log_2 n)$$.
- **속성**: 
  - 모든 노드는 유일한 키를 가짐
  - 왼쪽 서브트리 키 < 루트 키 < 오른쪽 서브트리 키
  - 양쪽 서브트리 모두 BST
- **성능**: 트리 모양에 따라 크게 달라짐. 편향된 경우 $$O(n)$$으로 저하.

### BST 연산
- **키로 탐색**: 평균 $$O(\log_2 n)$$
- **값으로 탐색**: $$O(n)$$ - 모든 노드 확인 필요
- **최소/최대 탐색**: 가장 왼쪽/오른쪽 경로 따라감
- **삽입**: $$O(\log_2 n)$$ - 탐색 경로를 따라가서 실패 지점에 삽입
- **삭제**: 3가지 경우로 가장 복잡:
  - 경우 1: 리프 노드 - 단순 제거
  - 경우 2: 한 개의 자식 - 자식을 부모에 연결
  - 경우 3: 두 개의 자식 - 후계자로 교체

### AVL 트리
- **목적**: $$O(\log_2 n)$$ 성능을 보장하는 자가 균형 이진 탐색 트리.
- **균형 인수**: 왼쪽과 오른쪽 서브트리의 높이 차이
- **제약**: 균형 인수는 -1, 0, 1 중 하나여야 함
- **재균형**: 균형 인수가 ±2가 되면 회전 사용
- **회전 종류**:
  - 단일 회전: LL, RR
  - 이중 회전: LR, RL

</details>
