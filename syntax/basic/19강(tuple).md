# Tuple ( 순서O, 중복O, 수정x, 삭제x ): primitive value

튜플형에서 알아두어야 할 것은 **수정, 삭제** 가 안된다는 점!!

primitive value이기 때문에 복사할 경우 primative한 성질을 가지고 있다. => 다음 강의에서...

```
a = ()
b = (1, )
c = (1, 2, 3, 4)
d = (10, 100, ('a', 'b', 'c'))
del c[2] # error
```

**Tuple 함수**
1. count(value): tuple 내의 value를 count
2. index(value): tuple 내의 value를 찾아 index 반환. => 없으면 **ValueError**





