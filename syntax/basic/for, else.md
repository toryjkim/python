# for else 문법
for문에도 else 문법이 존재한다.

특징: for 문 내에서 break가 실행되지 않으면 반복이 끝나고 else문이 실행된다. 

예제:
리스트에 홀수 값만 있는지 확인하기
```
l = [1, 3, 5, 7, 9, 11]

for num in l:
    if num % 2 == 0:
        break
else:
    print("Even value is not in the list")
```
