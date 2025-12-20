<details>
<summary>ENG (English Version)</summary>

## Chapter 10: Weighted Graph

### Weighted Graph
- **Definition**: A graph where each edge has an associated weight or cost.
- **Representation**: $$G = (V, E, w)$$
- **Path Length**: Sum of weights along path

### Minimum Spanning Tree (MST)
- **Definition**: A spanning tree with the minimum possible total edge weight.
- **Properties**: n-1 edges, no cycles, connects all vertices
- **Applications**: Communication networks, road networks, circuit design

### MST Algorithms
- **Kruskal's Algorithm**:
  - Strategy: Sort edges by weight, add if no cycle created
  - Time Complexity: $$O(e \log e)$$
  - Uses Union-Find for cycle detection
  - Better for sparse graphs
- **Prim's Algorithm**:
  - Strategy: Start with vertex, expand tree by adding minimum weight edge
  - Time Complexity: $$O(n^2)$$
  - Better for dense graphs

### Shortest Path
- **Definition**: Path with minimum total weight between vertices
- **Applications**: Navigation, network routing, resource optimization

### Shortest Path Algorithms
- **Dijkstra's Algorithm**:
  - Purpose: Single-source shortest path to all vertices
  - Strategy: Greedy approach, always select minimum distance vertex
  - Time Complexity: $$O(n^2)$$
  - Constraint: Non-negative edge weights
  - Maintains dist array and found set
- **Floyd-Warshall Algorithm**:
  - Purpose: All-pairs shortest path
  - Strategy: Dynamic programming with intermediate vertices
  - Time Complexity: $$O(n^3)$$
  - Formula: $$A^k[i][j] = \min(A^{k-1}[i][j], A^{k-1}[i][k] + A^{k-1}[k][j])$$
  - Handles negative weights (but not negative cycles)

### Algorithm Comparison
- **Kruskal vs Prim**: Kruskal better for sparse graphs, Prim for dense graphs
- **Dijkstra vs Floyd-Warshall**: Dijkstra for single source, Floyd-Warshall for all pairs

</details>

<details>
<summary>KOR (한국어 버전)</summary>

## 10장: 가중치 그래프

### 가중치 그래프
- **정의**: 각 간선에 가중치나 비용이 할당된 그래프.
- **표현**: $$G = (V, E, w)$$
- **경로 길이**: 경로를 따라가는 가중치의 합

### 최소 신장 트리 (MST)
- **정의**: 가능한 총 간선 가중치가 최소인 신장 트리.
- **속성**: n-1개 간선, 사이클 없음, 모든 정점 연결
- **응용**: 통신 네트워크, 도로 네트워크, 회로 설계

### MST 알고리즘
- **크루스칼 알고리즘**:
  - 전략: 간선을 가중치 순으로 정렬, 사이클을 형성하지 않으면 추가
  - 시간 복잡도: $$O(e \log e)$$
  - Union-Find로 사이클 탐지
  - 희소 그래프에 적합
- **프림 알고리즘**:
  - 전략: 한 정점에서 시작하여 최소 가중치 간선을 추가하며 트리 확장
  - 시간 복잡도: $$O(n^2)$$
  - 밀집 그래프에 적합

### 최단 경로
- **정의**: 두 정점 사이의 총 가중치가 최소인 경로
- **응용**: 내비게이션, 네트워크 라우팅, 자원 최적화

### 최단 경로 알고리즘
- **다익스트라 알고리즘**:
  - 목적: 단일 출발점에서 다른 모든 정점까지의 최단 경로
  - 전략: 탐욕 방식, 항상 최소 거리 정점 선택
  - 시간 복잡도: $$O(n^2)$$
  - 제약: 음수 간선 가중치 불가
  - dist 배열과 found 집합 유지
- **플로이드-워셜 알고리즘**:
  - 목적: 모든 정점 쌍 간의 최단 경로
  - 전략: 중간 정점을 이용한 동적 프로그래밍
  - 시간 복잡도: $$O(n^3)$$
  - 공식: $$A^k[i][j] = \min(A^{k-1}[i][j], A^{k-1}[i][k] + A^{k-1}[k][j])$$
  - 음수 가중치 처리 가능 (음수 사이클 제외)

### 알고리즘 비교
- **크루스칼 vs 프림**: 희소 그래프는 크루스칼, 밀집 그래프는 프림이 유리
- **다익스트라 vs 플로이드-워셜**: 단일 출발점은 다익스트라, 모든 쌍은 플로이드-워셜

</details>
