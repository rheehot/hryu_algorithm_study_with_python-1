## itertools

순열, 조합, product를 구현하거나 사용해야 할 때 사용

### combinations
조합 표현할 때 사용되는 메소드   
한 리스트에서 중복을 허용하지 않고 모든 경우의 수를 구하는 것  

~~~
from itertools import combinations

_list = [1, 2, 3]
combi = list(combinations(_list, 2))
print(combi) # [(1, 2), (1, 3), (2, 3)]
# 갯수 별로 조합을 반복할 수 있다.
for i in range(1, len(_list) + 1):
    print(list(combinations(_list, i)))
# [(1,), (2,), (3,)]
# [(1, 2), (1, 3), (2, 3)]
# [(1, 2, 3)]
~~~

### permutations
순열 표현할 때 사용되는 메소드
한 리스트에서 중복을 허용하고 모은 경우의 수를 구하는 것  

~~~
from itertools import permutaions

_list = [1, 2, 3]
perm = list(permutations(_list, 2))
print(perm)
# [(1, 2), (1, 3), (2, 1), (2, 3), (3, 1), (3, 2)]
~~~

### product
데카르트 곱이라고도 하는 cartesian product를 표현할 때 사용하는 메소드  
(DB의 join, 관계 대수의 product를 생각하면 된다)  
이 메소드의 특징은 두 개 이상의 리스트의 모든 조합을 구할 때 사용  

~~~
from itertools import product

_list = ["012", "abc", "!@#"]
pd = list(product(*_list))

# [('0', 'a', '!'), ('0', 'a', '@'), ('0', 'b', '!'), ('0', 'b', '@'), ('1', 'a', '!'), ('1', 'a', '@'), # ('1', 'b', '!'), ('1', 'b', '@')]

~~~

### 주의할 점

~~~
from itertools import combinations

_list = range(4)
combi = combinations(_list, 2)
print(list(combi))		# [(0, 1), (0, 2), (0, 3), (1, 2), (1, 3), (2, 3)]
print(list(combi))		# []
~~~


[참고](https://velog.io/@davkim1030/Python-%EC%88%9C%EC%97%B4-%EC%A1%B0%ED%95%A9-product-itertools)