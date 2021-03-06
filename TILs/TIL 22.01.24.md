# TIL 22.01.24

## 변화량 배열

좌표계를 확인하고 입력값에 따른 좌표 변화량을 적용할 수 있도록 만드는 배열

제일 처음에 문제가 나오면, 내가알고있는 형태의 좌표계인가? 각각의 좌표값들이 
어떤것이 열이고 어떤것이 행인지도 파악을해야한다. 문제가 좌표를 꼬아 낼수도있기 때문
> 일반적인 수학 좌표계와는 다를 경우가 있다. 그래서 x,y보단 row,column같이 명확하게 알수있는 변수로 나타내는 편이 좋다. `arr[r][c]`

```python
arr =[
  [0,0,0,0],
  [0,0,0,0],
  [0,0,0,0]
]

arr2 = [[0] * M for _ in range(N)]
```

기준접을 중앙응로 상하좌우 위치에가다 순서대로 1234 저장하기

```python
# 현재위치
r,c = [0,0]

# 상 하 좌 우
dr = [-1,1,0,0]
dc = [0,0,-1,1]

# 상 우 하 좌
dr = [-1,0,1,0]
dc = [0,1,0,-1]

# 8방향 시계방향 작성

dr = [-1, -1, 0, 1, 1, 1, 0, -1]
dc = [0, 1, 1, 1, 0, -1, -1, -1]

# 위로 이동하기 위한 rc의 변화량
r + dr[0], c + dc[0]
# 아래
r + dr[1], c + dc[1]
# 왼쪽
r + dr[2], c + dc[2]
# 오른쪽
r + dr[3], c + dc[3]

# 반복문으로 나타내면

num = 1

for i in range(4):
    next_row = r + dr[i]
    next_col = c + dc[i]
    # next_row와 next_col이 정상적일때만 집어넣고 싶다.
    if 0 <= next_row < 3 and 0 <= next_col < 4:
        arr[next_row][next_col] = num
        num += 1

for row in arr:
    print(row)
```

### 이동 방향을 결정

```python
r ,c = 5,5
# dir = 0 : 위, 1: 아래, 2: 왼쪽, 3: 오른쪽
dir = 0

# 이동방향 결정
dr = [-1,0,1,0]
dc = [0,1,0,-1]
num = 1
while 0 <= r < < 10 and 0 <= c < 10>:
    arr[r][c] = num
    r += dr[dir]
    c += dc[dir]

```

## 메서드

메서드에서 중요한건 입력값이 어떻게 들어가고 반환값이 어떻게 나오는지 숙지하고 있는것이다. 

메서드 이름으로 유추하는 방법도 있는데 .is~()와 같이 인지 아닌지 판단하는 is로 시작하는 메서드는 bool값을 반환한다고 유추할 수 있다.

### 문자열 변경 메서드

문자열 변경은 immutable 인데 바뀐 문자열을 반환하는 함수를 이용해 문자열을 바꾸듯 사용할 수 있다.

여러 메서드들을 어느정도 외워 두는게 좋을것같다..

## 예외처리

condition : 내가 작성한 조건문이 모든 조건을 커버하는가, 내가 전부 파악하고 있는가.

for : 반복문 원하는 횟수가 맞는지, 반복문 값 진입과 결과가 맞는지?

while : for문에 더해서 종료 조건이 제대로 되었는지

function : 호출이 제대로 되었는지, 파라미터로 제대로 전달이 되었는지, 결과가 원하는대로 나오는지, type 

알고리즘은 몇천문제씩 동일한 문제, 비슷한 유형의 문제를 풀어봐야 한다.

### 디버깅

로직 에러 발생시
* 명시적인 에러 메시지 없이 예상 결과가 다른 경우

  * 정상적 동작 코드 이후 작성된 코드 생각
  * 전체 코드를 살펴본다.
  * 휴식을 가져본다.
  * 누군가(오리)에게 설명해본다.


try except문 작성시 except 문중 가장 포괄적인 예외는 마지막에 넣는것이 좋다.