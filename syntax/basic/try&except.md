# try & except

## 에러종류:
1. SyntaxError: 잘못된 문법
2. NameError: 참조변수 없음
3. ZeroDivisionError: 0으로 나눔
4. indexError: 접근할 수 있는 index 범위를 넘어감
5. keyError: key가 없을 때
6. AttributeError: 모듈, 클래스에서 잘못된(없는) 속성 사용시
7. ValueError: 값이 없을 때
8. FileNotFoundError: 파일이 없을 때
9. TypeError: 이 타입이 행할 수 없는 어떤 것을 수행했을 때, ex) str+int / str()

## 문법
1. try: 에러가 발생할 가능성이 있는 코드를 이 안에 작성
2. except: 모든 에러를 잡아내어 내부에 작성한 코드를 실행함.
3. except specificError: 특정에러가 발생했을 때만 코드를 실행함.
4. else: 에러가 발생하지 않았을 때
5. finally: 무조건 실행되는 문장.
