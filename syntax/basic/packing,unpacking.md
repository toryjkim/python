# packing
## `*args, **kwargs`

함수에서 packing이란 여러개의 값을 하나의 tuple or dict형으로 만들어주는 방법이다.

1. 여러개의 값을 입력한 경우 `*args`와 같이 매개변수 앞에 `*`을 붙이면 입력받은 모든 값을 packing해서 tuple 형으로 만들어준다.
```
def args_func(*args):
  print(args)
  
args_func('Kim', 'Park') # ('kim', 'park')
```

2. 여러 개의 값을 key = value 형태로 입력한 경우 `**kwargs`와 같이 매개변수 앞에 `**`을 붙이면 입력받은 모든 값을 packing해서 dict 형으로 받을 수 있다.
``` 
def args_func(**kwargs):
  print(kwargs)
 
args_func(fname = 'Judy', lname = 'kim') # fname : 'Judy', lname : 'kim'}
```


## `*args, **kwargs`를 혼합해서 사용하면

일반 매개변수, `*args`, `**kwargs` 순서를 꼭 맞춰 주어야 한다.
```
def args_kwargs(fullname, *args, **kwargs):
  print(fullname)
  print(args)
  print(kwargs)

args_kwargs('JudyKim', 'Judy', 'Kim', fname = 'Judy', lname = 'kim')
```

# unpacking
1. list 앞에 `*`을 붙이면 list 내부의 모든 값을 반환한다. 
```
def args(*args):
  print(*args)
  
args('Judy', 'kim') # Judy kim
```

2. dict형 앞에 `**`을 붙일 경우 key = value 형태로 모든 값을 반환한다.
```
def kwargs(**kwargs):
  print(kwargs)

person = {
  fname : 'Judy',
  lname : 'Kim'
}
kwargs(**person) # {fname: 'Judy', lname: 'Kim'}
```
