# 딕셔너리

## 1. 특징:
배열의 단점은 원하는 값을 찾기위해 index 번호를 알고 있어야 한다는 점이다.
예를들어 list 안에 "Tory"라는 값이 저장되어 있다면 "Tory"가 몇번 index에 저장되어 있는지 탐색하는 과정이 필요한다.
아래 예시처럼 말이다.

```
l = [["Judy","01093920000"], ["Tory","01080810000"]]

for i in range(len(l)):
    if l[i][0] == "Tory":
        print(l[i][1]) 
```

반면 딕셔너리는 key를 value의 형태로 저장한다. index를 찾을 필요없이 바로 data에 접근할 수 있다.
```
l = {'Judy': '01093930000', 
    'Tory': '01080810000'}
```

배열에 데이터를 저장할 때 key와 value의 형태로 저장하는 것이 용이하다면(ex. 전화번호부, css 키워드, module 등) 딕셔너리가 모든 연산과정에서
유리하다.


## 2. 함수:
1. keys(): key들을 dict_keys 형으로 반환한다. => list와 같은 iterable 형으로 형변환 필요
2. values(): value들을 dict_values 형으로 반환. => list와 같은 iterable 형으로 형변화 필요
3. items(): [(key, value)] 구조로 dict_items 형으로 반환. => iterable 형으로 형변환 필요
    
