# TIL 22.01.18

알고리즘 문제를 풀면서 `list.sort()`함수의 인자중 `key`값을 `lamda`로 적용해 풀어보았다.

람다식에 관해서도 조금더 알게 되었다.

## python

파이썬실습을 하면서 문자열 재거에 대해서 배워볼수 있었다. 구글링을 통해 알게된 것은
`replace()` 인데 첫 번째 인자를 전부 두 번째 인자로 치환한다. 
스트링 관련 내장함수도 알아봐야겠다.
### 'a'가 싫어


> 입력으로 짧은 영단어 word가 주어질 때, 해당 단어에서 'a'를 모두 제거한 결과를 출력하시오.

---
```
[입력 예시]
apple

[출력 예시]
pple
```

```pyhon
word = input()

print(word.replace('a', ''))
```


## BOJ

팰린드롬 문제 2문제를 풀어보았다. 각각 b2, s5문제였는데 s5문제도 버겁다..
로직이 틀린것 같다. 중복하여 고르지 않게 이중 포인터 비슷하게 2중포문으로 구현한거같은데.. 왜 안풀리는지 알수 없다.

## from itertools import combinations

itertools라이브러리를 사용하면 combinations 함수를 사용할 수 있는데, words 리스트의 값들을 정수로 들어오는 두번째 인자의 갯수만큼 조합해 만들수 있는 모든 경우의 수를 반환한다. 

문자열 조합 만들때 사용해 보았다. 

`combination = list(combinations(words, 2))` 