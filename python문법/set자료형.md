### 1. set 집합
- 순서 없고, 중복 허용x
- 변하는 값은 가질 수 없다

### 2. 선언
~~~
>>> s = {}
>>> type(s)
<class 'dict'>
>>> s = set()
>>> type(s)
<class 'set'>
>>> s
set()
~~~
- set 생성자에 iterable한 객체를 넣으면 변환하여 set 만들어 준다
- 몰론, set생성자 없이 바로 중괄호 안에 값을 넣어도 된다
~~~
>>> s = set([1,3,5,7])
>>> s
{1, 3, 5, 7}
>>> p = {1, 3, 5, 7}
>>> p
{1, 3, 5, 7}
~~~
### 3, set 의 in
~~~
>>> 2 in r
True
>>> 3 in r
False
>>> 3 not in r
True
~~~
### 4. set의 원소 추가/수정/제거
- add : k.add(50)
- update : k.update([3, 4, 5])
- remove