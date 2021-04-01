## deque

보통 queue는 FIFO방식

deque는 양방향 큐로,  앞뒤 양쪽 방향에서 원소 추가하거나 제거 가능

deque는 양 끝 원소의 append와 pop이 압도적으로 빠르다

컨테이너의 양끝 원소에 접근하여 삽입 또는 삭제 할 경우, 일반적인 리스트가 이러한 연산에 O(N)이 소요되는 반면, **deque는 O(1)로 접근 가능** 



~~~
from collections import deque

deq = deque()

# 앞에 원소 추가
deq.appendleft(10)

# 끝에 원소 추가
deq.append(0)

# 앞에 원소 삭제
deq.popleft()

# 뒤 원소 삭제
deq.pop()
~~~



rotate() 메서드 ->  양수 값 또는 음수 값 파라미터로 제공하여 deque를 좌우로 회전 가능

~~~
deq = deque([1, 2, 3, 4, 5])
deq.rotate(1)
print(deque)
# [5, 1, 2, 3, 4]

deq.rotate(-1)
print(deq)
# deque([1, 2, 3, 4, 5])
~~~



## deque  왜 ? 언제 ? 사용..?

deque는 스택 처럼, 큐 처럼 사용 가능

시작점 끝점 연산에서 최적화된 연산 속도 제공

deque는 list보다 빠르다

deque는 push/pop 빈번할때 사용하면 좋다

-> 백준 7576 토마토 : deque 사용 시간초과 안뜸



[참고](https://chaewonkong.github.io/posts/python-deque.html)