# 집합(set) 순서x, 중복x

문법: set()

```
a = set([1, 2, 3, 4])
b = {1, 2, 3, 3}
print(type(a), type(b)) # set, set
print(b) # 1, 2, 3 => 중복 x
```

## 함수:
1. intersection(&): 교집합
2. unione(|): 합집합
3. difference(-): 차집합
4. add(value): 값 추가
5. remove(value): 값 제거 # 없으면 Key error
