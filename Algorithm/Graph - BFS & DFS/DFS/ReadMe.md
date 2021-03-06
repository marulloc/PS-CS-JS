# DFS 깊이 우선 탐색

- Graph 자료구조를 순회하는 알고리즘
- 여러가지 일들이 있고, 그 일들 사이에 **선행관계** 가 있을 때 사용한다.
- Stack을 이용한다. 선행관계를 따질 때, Stack은 **발자취**가 된다. 막힌 길에서 돌아가기 위한 수단
- 하나의 노드는 한 번 방문한다. Stack을 통해 되돌아 갈 때는 방문이라고 여기지 않음

### logic

1. 나를 먼저 방문
2. 내 주변의 인접 노드를 확인해서 아직 방문하지 않은 노드로 향한다.

- 따라서, 방문 여부를 알기 위한 배열이 필요하다.
- 또한, 인접 노드 중, 어떤 노드를 먼저 방문할지의 로직이 필요하다.

### So,

- Graph를 위한 2차원 배열이 필요하다. 공간 복잡도를 최적화하기 위해 2차원 **vector**를 사용하자.
- **방문 여부를 알기 위한 1차원 배열**이 필요하다.
- 발자취를 남길 Stack 필요하다. -> Stack을 따로 두지 말고, Stack 로직을 따르는 **재귀함수**를 이용하자.

### O(V+E)

- 모든 노드를 방문하는 것 O(V)
- 모든 노드에서, 간선의 갯수만큼 for문을 돌린다.
  - 인접 행렬로 그래프를 구현하면, 시간복잡도가 일정하다.
  - 인접 리스트로 그래프를 구현하면, 간선의 갯수만큼 for문을 돌리므로 O(E)

따라서 시간복잡도는 O(V+E)다.
