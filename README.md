<details>
<summary>ENG (English Version)</summary>

## Chapter 9: Graph

### Graph
- **Definition**: A data structure representing relationships between connected objects (vertices/nodes) via edges.
- **Notation**: $$G = (V, E)$$
  - $$V(G)$$: set of vertices
  - $$E(G)$$: set of edges
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

</details>

<details>
<summary>KOR (한국어 버전)</summary>

### 그래프
- **정의**: 연결된 객체(정점/노드)들 간의 관계를 간선으로 표현하는 자료구조.
- **표기**: $$G = (V, E)$$
  - $$V(G)$$: 정점의 집합
  - $$E(G)$$: 간선의 집합
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

</details>
