# TIL 22.02.16


## 알고리즘

큰 값을 찾는 조건문, 그리고 반례에 좀더 신경써야 겠다.. 점점 퇴화하는 기분이 든다. 

kmp 문자열 탐색 알고리즘과 보이어 무어에 대해서 알게 되었다. 처음에는 정말 이해가 안갔지만 최대한 검색을 통해 이해하려고 했고 이해는 했다. 구현은 다른 이야기..

### kmp

문자열을 탐색할때 찾고자하는 문자열의 일치하는 패턴을 찾아 틀릴시 돌아갈 지점의 배열을 따로 생성해 문자열을 찾는 알고리즘이다. 내가 가진 문자열에 반복되는 부분이 있다면 그만큼을 뛰어 넘고 검색을 할 수 있을까? 에서 시작되는 알고리즘이다.

### 보이어 무어

문자열을 배열에 넣고 주어진 문자열에서 존재하는지 안하는지 찾아 이동하는 알고리즘이다. 