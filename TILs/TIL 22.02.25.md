# TIL 22.02.25

## BFS

너비 우선탐색에 대해서 배웠다. !

# 너비 우선 탐색(Breadth-First Search)

BFS란 특정 노드에서 시작해서 인접한 노드를 먼저 탐색하는 방법이다. 시작 정점으로부터 가까운 정점을 먼저 방문하고 멀리 떨어져 있는 정점을 나중에 방문하는 순회방법

- 두 노드사이의 최단경로, 임의의 경로를 찾고 싶을 때 사용
- 재귀적으로 동작하지 않는다
- 어떤 노드를 방문했었는지 여부를 검사해야 한다.
- 큐를 사용한다 → FIFO(First In First Out)

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/cbfb4f2e-eb46-404d-abaf-818ac5bb2928/_2021-05-06__4.31.17.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220226%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220226T140126Z&X-Amz-Expires=86400&X-Amz-Signature=7aab7d427ef688b704f5071b547f6897e7d26ce74292a4903b8467a22f03e1d6&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22_2021-05-06__4.31.17.png%22&x-id=GetObject)

- 장점
    - 출발노드에서 목표노드까지의 최단 길이 경로를 보장한다.
- 단점
    - 경로가 매우길 경우에는 탐색 가지가 급격히 증가함에 따라 보다 많은 기억 공간을 필요로 하게 된다.→ 공간요구