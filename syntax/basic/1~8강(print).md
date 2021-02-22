# print 함수의 이해

## 1. 옵션 사용해 보기

### 1.1. seperator 옵션
print 함수 내부에 sep argument로 문자열을 입력하면 그 문자열이 출력될 값을 나누는 기준이 된다. (defalut = ' ') 
```
# default
print('This', 'is', 'print', 'of', 'Python') # This is print of Python

# sep = '' => 공백 제거
print('This', 'is', 'print', 'of', 'Python', sep='') # ThisisprintofPython

# sep = '-' => 날짜형식
print('2021', '02', '20', sep='-') # 2021-02-20
```

### 1.2. end 옵션
print 함수는 출력의 끝에 항상 \n(줄바꿈) 문자를 포함한다. 이때 end 옵션을 사용하면 문자의 끝에 \n 대신 다른 문자를 포함하여 출력할 수 있다.

```
# default
print('first line') 
print('second line')

출력
### 
first line
second line
###

# end = '' => 줄바꿈 제거
print('first line, ', end='')
print('still first line')

출력
###
firt line, still first line
###
```

### 1.3. format method
string 값은 format이라는 메소드를 가지고 있다.
이 메소드를 사용하면 조금 더 편리하게 원하는 문자열을 출력할 수 있다.

```
print('start using {}'.format('string format method')) # start using string format method

print('{} and {}'.format('A','B')) # A and B

print('{1} is the next letter {0}'.format('A', 'B')) # B is the next letter A

print('{b} is the next letter {a}'.format(a='A', b='B')) # B is the next letter A

# %s: 문자, %d: 숫자, %f: 실수, %
print("{:s}'s age is {:d}".format('Yeong', 29)) # Yeong's age is 29
print("{number:4.2f}".format(number=4933.125)) # 4933.12 5 미만은 반내림
print("{number:4.2f}".format(number=4933.12501)) # 4933.13   5 이상은 반올림
```

구문법
```
print("%s's age is %d" % ('Yeong', 29)) # Yeong's age is 29
print("%.2f" % ( 29.5 )) # 29.50 
```

### 1.4. Escape code
Escape code는 어떠 문자를 타이핑하지 않고 문자를 출력해야할 때 사용할 수 있는 방법이라고 생각하면 된다.

```
\n : 개행
\t : 탭
\' : \ 뒤의 문자를 그대로 출력 (')
\\ : \ 문자 출력
\r : carriage return : 커서를 앞으로 이동시킨다.
\f : form feed 새로운 페이지부터 문자열을 출력한다. (carriage return이 자동으로 실행된다.)
\a: 벨 소리
\b: 백 스페이스
\000: 8진수의 값을 000에 입력하면 해당하는 Ascii 값을 출력한다.
```

- 테스트 해보기
```
print("'You'")
print("""'You'""")
print("\'You\'") # \뒤의 문자는 그대로 출력됨
print('"You"')
print('\\You\\')
print('', end='\n\n')
print('\t\t Tan')
print('Hello\rWorld') # \r를 기준으로 커서가 맨 앞으로 이동하기 때문에 World만 출력됨
print('123\f'456) # \f를 기준으로 다음 라인에서 시작. # 123
                                                    #    456
print('Hello\bWorld')
print('\110\145\154\154')

#출력
###
'You'
'You'
'You'
"You"
\You\


                 Tan
World


HellWorld
Hell
###
```

### 참고
[python-string-format](https://www.w3schools.com/python/ref_string_format.asp)

[python-escape-characters](https://www.w3schools.com/python/gloss_python_escape_characters.asp)
