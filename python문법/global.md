## 전역변수 global
- 함수 안에서 global로 전역변수 선언
- 함수 밖에서 global 선언했어도 함수 안에서 또 선언/ 그렇게 안해주면 지역변수로 처리됨

~~~ 
global a a = 1

def test(): 
    global a 
    a = 3 
    b = 2
    return a + b

print(test())
print(a)
~~~

- 함수안 글로벌 변수 지우면 a=1이됨