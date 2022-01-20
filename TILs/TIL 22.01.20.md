# TIL 22.01.20 

## 재귀 

```python 
# 모든 부분집합 : 멱집합
# [1,2,3] >> 1 2 3 12 13 23 123 ''
# [0, 0, 0] : selected 각 요소가 부분집합에 포함되는지 여부를 표시하는 배열
# idx : 포함여부 결정할 요소 인덱스

N = 3
arr = [1, 2, 3]
selected = [0, 0 ,0]
def ps(idx):
    if idx == N: # 모든 요소의 포함여부 결정, 인덱스 벗어남
        for i in range(N):
            if selected[i]:
                print(arr[i],end="")
        print()
        return
    selected[idx] = 1 # idx 번째 요소가 부분집합에 포함
    ps(idx + 1)
    selected[idx] = 0 # idx 번째 요소가 부분집합에 미포함
    ps(idx + 1)
