<details>
<summary>ENG (English Version)</summary>

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

</details>

<details>
<summary>KOR (한국어 버전)</summary>

### 큐
- **구조**: 선입선출(FIFO) 자료구조.
- **연산**: 뒤(rear)에서 삽입, 앞(front)에서 삭제.

### 큐 응용
- 버퍼, 통화 대기열, 인쇄 작업 큐, 실시간 비디오 스트리밍, 시뮬레이션(은행 대기표, 공항 활주로).

### 큐 구현
- **선형 큐**: 리스트를 사용한 간단한 구현.
- **원형 큐**:
  - 고정 크기 배열에서 `front`와 `rear` 포인터를 관리.
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

</details>
