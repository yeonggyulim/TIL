# 응용 자료구조

## 1. 스택(Stack): LIFO

## 2. 큐(Queue): FIFO
     
## 3. 트리(Tree): 계층형 자료구조(Hierarchical Data Structure)
    - 이진 트리(Binary Search Tree)
    - 힙(Heap): 완전 이진 트리에 있는 노드 중 키값이 가장 큰 노드나 작은 노드 찾기 위해 만든 자료구조
     - 최대 힙(Max Heap): 키 값이 가장 큰 노드 찾기 위한 힙 (부모노드의 키값 >= 자식노드의 키 값)
     - 최소 힙(Min Heap): 키 값이 가장 작은 노드 찾기 위한 힙 (부모노드의 키값 <= 자식노드의 키 값)

## 4. 그래프(Graph)
     - 연결되어있는 원소 간의 관계를 표현하는 자료구조
     - 연결할 객체 나타내는 정점(Vertex)과 객체 연결하는 간선(Edge)의 집합으로 구성
     - G = (V, E)
     - 그래프의 종류
          - 무방향 그래프(Undirected Graph)
          - 방향 그래프(Directed Graph)
          - 완전 그래프(Complete Graph)
          - 부분 그래프(Subgraph)
          - 가중 그래프(Weight graph, Network)
     - 그래프 관련 용어
          - Adjacent(인접): 두 정점(Vertex) 사이에 연결된 간선(Edge)이 있을 때, 두 정점은 인접하다.
          - Incident(부속): 두 정점(Vertex) 사이에 연결된 간선(Edge)이 있을 때, 간선은 두 정점에 부속되어 있다.
          - Degree(차수): 정점에 부속되어 있는 간선의 수, in-degree + out-degree
          - Path(경로): 그래프에서 간선을 따라 갈 수 있는 길을 순서대로 나열한 것 ex) A-B-C, 경로 길이: 2
          - Simple Path(단순 경로): 모두 다른 정점으로 구성된 경로
          - Cycle(사이클): 경로의 시작 정점과 마지막 정점이 같은 단순 경로
          - DAG(Directed Acyclic Graph): 방향 그래프이면서 사이클이 없는 그래프
          - Connected(연결): 두 정점 사이에 경로가 있으면 연결되었다고 한다.
          - Connected Graph(연결 그래프): 서로 다른 모든 쌍의 정점들 사이에 경로가 있는 그래프 ex) 트리: 사이클이 없는 연결 그래프
          - Disconnected Graph(단절 그래프): 연결되지 않은 정점이 있는 그래프
     - 그래프 순회(Graph Traversal) 또는 그래프 탐색(Graph Search)
          - DFS(깊이 우선 탐색): LIFO인데, 보통 스택 안쓰고 Recursive 사용함
          - BFS(너비 우선 탐색): FIFO로 보통 Queue 사용함
     - 신장 트리(Spanning Tree)
          - 그래프 관점에서 트리는 사이클이 없는 단순 연결 그래프
          - 신장 트리 : n개의 정점으로 이루어진 무방향 그래프 G에서 n개의 모든 정점과 n-1개의 간선으로 만들어진 트리
          - 최소의 간선을 이용하여 모든 정점을 연결한 그래프 ex) 최소의 도로를 사용하여 모든 도시 연결해야하는 도로망 건설
          - Depth First Spanning Tree(깊이 우선 신장 트리)
          - Breadth First Spanning Tree(너비 우선 신장 트리)
          - Minimum Cost Spanning Tree(최소 비용 신장 트리) ex) Kruskal 알고리즘, Prime 알고리즘 주로 사용
          
          
