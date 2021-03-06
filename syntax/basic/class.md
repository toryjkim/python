# class

## 1. 기본 문법:
```
class Name:
  # 변수
  # 메소드
```

## 2. 특징
1. 인스턴스는 개별적인 공간을 가지고 있어서 공유하지않는 고유의 변수를 가지고 있다.
```
class User:
    def __init__(self, name):
        self.name = name
        
user1 = User("Judy")
user2 = User("Tory")
print(user1.name) # Judy
print(user2.name) # Tory
```
2. 클래스는 인스턴스가 모두 공유하는 변수 및 함수를 가지고 있다.
- 인스턴스가 어떤 변수를 호출할 때 개별 변수를 가지고 있다면 그 값을 반환하지만, 그렇지 않다면 클래스에 해당 변수를 확인해서 있다면 반환한다. 
```
class User:
    a = True
    def __init__(self, name):
        self.name = name
        
user1 = User("Judy")
user2 = User("Tory")

print(user1.a) # True
print(user2.a) # True

```
2-1. 인스턴스변수가 없고 클래스변수만 있을 때 인스턴스에서 클래스변수를 직접적으로 접근해서 수정할 수 없다.
- 새로운 인스턴스변수가 생성된다
```
class User:
    a = True
    def __init__(self, name):
        self.name = name
        
user1 = User("Judy")
user2 = User("Tory")

user1.a = False
print(user1.a) # False
print(user2.a) # True
```
2-2. 클래스 변수를 수정하고 싶다면 클래스 변수를 통해 접근해야 한다.
```
class User:
    a = True
    def __init__(self, name):
        self.name = name
        
user1 = User("Judy")
user2 = User("Tory")

User.a = False
print(user1.a) # False
print(user2.a) # False
```

## 상속, 다중 상속:
### 상속 문법
super()를 통해 부모를 호출할 수 있다. (init과 같이 부모가 실행될 때 무조건 실행되는 매소드는 super로 꼭 부모를 호출해야 한다.)
```
class Car():
    """Parent class"""
    def __init__(self, type, color):
        self.type = type
        self.color = color
        
class BmwCar(Car):
    """Sub Class"""
    def __init__(self, name, type, color):
        super().__init__(type, color)
        self.name = naem
    def show_model(self) -> None:
        ruturn "Your Car Name : %s" % self.name
```
### 특징
1. 서브클래스가 부모클래스의 클래스 변수를 상속 받을 때, 부모클래스의 클래스 변수를 공유한다.
```
class Car():
    a = 0
    """Parent class"""
    def __init__(self, type, color):
        self.type = type
        self.color = color
        a += 1
        
class BmwCar(Car):
    """Sub Class"""
    def __init__(self, name, type, color):
        super().__init__(type, color)
        self.name = name
    def show_model(self) -> None:
        return "Your Car Name : %s" % self.name

bmw = BmwCar("cs-100", "suv", "white")
print(BmwCar.a) # 1
print(Car.a) # 1
```
### 상속정보 확인
mro 메소드
```
print(BmwCar.mro()) # BmwCar, Car, Object
```

### 다중상속
```
class A:
    pass
class B:
    pass
class C(A,B):
    pass
class D(C):
    pass
    
print(D.mro()) # D, C ,A ,B
```
        










