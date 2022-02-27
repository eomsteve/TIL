# dfs, bfs, 스택, 큐

# 스택(Stack)

한 쪽 끝에서만 자료를 넣고 뺄 수 있는 LIFO(Last In First Out)구조

## 스택의 연산

- push(item) 삽입 : 스택에 자료를 넣음
- pop() 삭제 : 스택의 자료를 제거
- top() = peak 읽기 : 스택의 맨 위 요소 반환
- empty() : 스택이 비어있는지 확인

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/55ccb6cc-fb3a-4bff-b5b9-5c0049e5bc2f/Untitled.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/55ccb6cc-fb3a-4bff-b5b9-5c0049e5bc2f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220227%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220227T050050Z&X-Amz-Expires=86400&X-Amz-Signature=6d3e1aed8371a1f2b546455e18a7b90e471286c0207923c6c6ce001dc2e62542&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

## 시간복잡도

- 삽입/ 삭제 : $O(1)$ 맨 위 원소 접근만 하면 된다.
- 검색 : $O(n)$ 탐색을 하려면 원소를 하나하나 꺼내 확인해야 한다.

## **Stack의 응용분야**

- 함수의 호출순서 제어
- 인터럽트가 발생하여 복귀주소를 저장할 때
- 후위 표기법(Postfix Notation)으로 표현된 수식을 연산할 때
- 재귀(Recursive)프로그램의 순서 제어
- 그래프의 깊이 우선 탐색 (DFS)


# 큐(Queue)

먼저 집어넣은 데이터가 먼저 나오는 FIFO(First In First Out) 구조로 저장하는 형식

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/320d035d-1f14-45aa-8ab8-f4733d838abb/Untitled.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/320d035d-1f14-45aa-8ab8-f4733d838abb/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220227%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220227T050159Z&X-Amz-Expires=86400&X-Amz-Signature=0b3059105f7a4ba2fa7d24956cae3cbef518d0d37254fbbb52e83fb085e0d755&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

## 큐의 연산

- push(item): 큐 데이터(item)삽입
- pop():큐 데이터 제거
- front(): 큐 맨앞 원소 데이터 반환
- back(): 큐 맨뒤 원소 데이터 반환
- empty():큐가 비어있는지 확인

## 시간복잡도

- 삽입/삭제 : 원소를 삽입 삭제하는 경우 $O(1)$
- 검색 :  탐색을 하려면 원소를 하나하나 꺼내 확인해야 한다. $O(n)$

## 선형큐

push가 될 때 rear(back) 포인터를 하나 증가시킵니다. 그리고 pop이 될 때마다 front 포인터를 증가하는 식으로만 구현을 한 걸 선형 큐

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3f8efb3b-f7fc-4a4e-8438-e2185e714911/_2021-05-06__3.00.46.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/3f8efb3b-f7fc-4a4e-8438-e2185e714911/_2021-05-06__3.00.46.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220227%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220227T050211Z&X-Amz-Expires=86400&X-Amz-Signature=9d37649b904e14a074900f25670eedb16fa9f11ad477e9a7de7c35f2082f9abd&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22_2021-05-06__3.00.46.png%22&x-id=GetObject)

큐에 데이터를 넣는 경우: 프론트는 고정, 리어가 추가되는 데이터를 가리키며 이동함

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c9238caa-6852-4426-99d5-130266ec4000/_2021-05-06__3.08.26.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c9238caa-6852-4426-99d5-130266ec4000/_2021-05-06__3.08.26.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220227%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220227T050236Z&X-Amz-Expires=86400&X-Amz-Signature=87004ae96c0ba5d06e1d3995b691c59a2465e91dbab9d99cda642331864bbfe2&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22_2021-05-06__3.08.26.png%22&x-id=GetObject)

데이터를 삭제시(Front가 고정):데이터가 삭제될 때 마다 데이터를 한칸씩 이동해야 한다.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/be9e889a-c01e-44d5-bc87-95f44a8b4514/_2021-05-06__3.01.11.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c9238caa-6852-4426-99d5-130266ec4000/_2021-05-06__3.08.26.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220227%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220227T050236Z&X-Amz-Expires=86400&X-Amz-Signature=87004ae96c0ba5d06e1d3995b691c59a2465e91dbab9d99cda642331864bbfe2&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22_2021-05-06__3.08.26.png%22&x-id=GetObject)

데이터를 삭제시(Rear가 고정) : 프론트의 포인터가 증가하며 내보낼 데이터를 순차적으로 가리킴 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8cfb3f43-32d7-423d-892e-865bae193ae4/_2021-05-06__3.42.23.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/8cfb3f43-32d7-423d-892e-865bae193ae4/_2021-05-06__3.42.23.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220227%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220227T050310Z&X-Amz-Expires=86400&X-Amz-Signature=ce47ce6aa9b80465065305012954da33f6d65841c8538bc4e2621a331514a92c&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22_2021-05-06__3.42.23.png%22&x-id=GetObject)

- 단점 : Rear가 배열의 끝까지 이동이 되면 더이상 새로운 데이터를 받을 수 없다. ⇒가득 찼다고 느끼기 때문
- 이런경우를 해결하려면 재정렬이 필요하다.

## 원형큐

선형큐의 단점을 보완하기 위해 만들어짐, 리어를 다시 첫번째를 가리키게 하여 저장공간을 순환적으로 사용함

- 데이터 삽입
    
    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/41c848c2-6941-4e43-bd88-c4efc13af48c/_2021-05-06__3.45.35.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/41c848c2-6941-4e43-bd88-c4efc13af48c/_2021-05-06__3.45.35.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220227%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220227T050341Z&X-Amz-Expires=86400&X-Amz-Signature=2187108e1415d91cccdef696b1f5897eb88bc6b7bed7c06328328424fbeb4074&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22_2021-05-06__3.45.35.png%22&x-id=GetObject)
    
- 데이터 삭제
    
    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/14f4a7ac-4791-432f-9893-ef959842cafd/_2021-05-06__3.46.02.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/14f4a7ac-4791-432f-9893-ef959842cafd/_2021-05-06__3.46.02.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220227%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220227T050353Z&X-Amz-Expires=86400&X-Amz-Signature=69e6b3768e5d56dd97fa3f65c1beae734e1d8e774c9f78bcfa162430e656b661&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22_2021-05-06__3.46.02.png%22&x-id=GetObject)
    
- 데이터 포화상태
    
    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/99dd49f7-fd33-4710-a553-c0e59fad03f0/_2021-05-06__3.54.10.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/99dd49f7-fd33-4710-a553-c0e59fad03f0/_2021-05-06__3.54.10.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220227%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220227T050406Z&X-Amz-Expires=86400&X-Amz-Signature=420001346e728c494639db3b0bbdc280b757ebc0bb6af4459a85601b7acd0809&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22_2021-05-06__3.54.10.png%22&x-id=GetObject)
    
    - 칸이 비어있는 이유 : 리어의 위치와 프론트의 위치가 같을 경우 빈 상태를 표현할 수 있는데 포화 상태도 같게 표현하면 비어있는지 포화인지 알 수가 없기 때문

## Queue의 응용분야

- 데이터를 순서대로 처리할 때
- BFS(너비 우선탐색) 구현 할 때

# 덱(Deque)

큐와 비슷하지만 큐는 front 에서만 삭제하고 back에서만 삽입하는데, 덱은 front 와 back 에서 삭제와 삽입이 모두 가능하다.큐의 장점과 스택의 장점을 합쳐놓은 자료구조이다.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/330f3a4d-b120-4a97-bc99-ff5ecaa469c9/Untitled.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/330f3a4d-b120-4a97-bc99-ff5ecaa469c9/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220227%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220227T050431Z&X-Amz-Expires=86400&X-Amz-Signature=79d3487399fa5960d4b7f5f5d346a80d24e6376f147cd3358f52aeb7b18bd0ef&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

## 특징

- 크기가 가변적이다
- 중간요소가 삽입, 삭제될 때 , 요소들을 앞/ 뒤로 밀 수 있으므로 vector보다 좋은 성능을 가지고 있다.
- 앞/뒤 삽입 삭제 성능은 좋지만 중간의 삽입/삭제 성능은 좋지 않다.

## 시간복잡도

- 삽입/삭제 : 원소를 앞,뒤에 삽입하는 경우 : $O(1)$
- 탐색 : 원소를 탐색하는 경우 $O(1)$  인덱스 접근

## 단점

- 중간에서 삽입 삭제가 어렵다
- 구현이 어렵다

## Deque 사용하는 곳

- 데이터의 개수가 가변적일경우
- 데이터 검색을 거의 하지 않을경우 ( 랜덤요소에 접근해야할 때)


### 그래프 인접 간선 배열 만들기

```python


```