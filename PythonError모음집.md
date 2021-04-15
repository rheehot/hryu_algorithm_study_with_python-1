## Runtime Error

#### 1. IndexError
​	존재하지 않는 index를 호출했을 때 발생

#### 2. NameError

​	아직 정의되지 않은 이름을 사용했을 때 발생

#### 3. TypeError

​	type에 지원되지 않는 명령 지시했을 때 발생

#### 4. Syntax Error

파이썬 상 문법이 틀렸을 때 발생하는 오류

- print에 괄호 넣지 않은 경우
- 괄호 안 닫은 경우..

#### 5. AttributeError

모듈, 클래스의 잘못된 속성 사용했을 때 발생

## 예외처리 기본 try-except-else-finally

- try : 에러 발생 가능성이 있는 코드 실행
- except : 에러 발생 시 (생략 가능, 여러개 사용 가능)
- else : 에러가 발생하지 않았을 경우 실행 (생략 가능)
- finally : 항상 실행 (생략 가능)

에러 종류를 명시해서  `except ValueError:` , `except NameError:` 이런 식으로 써도 되지만, 어떤 에러가 발생할지 모르겠을 때는 최종적으로 `except Exception:`사용 가능

