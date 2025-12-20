<details>
<summary>ENG (English Version)</summary>

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

</details>

<details>
<summary>KOR (한국어 버전)</summary>

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

</details>
