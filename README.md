//마크다운 사용법 정리 https://heropy.blog/2017/09/30/markdown/
//본인 벨로그 https://velog.io/@grapefruitgreen
<h1>1.그리디</h1>

<p>
  <h2>그리디란</h2>
현재 상황에서 가장 좋아 보이는 것만을 선택하는 알고리즘이다.</p><p>현재 상황에서 가장 좋아보이는 것만을 선택하기 때문에,
정확한 답을 도출하지 못하더라도 그럴싸한 답을 도출하는 데에 도움이 된다.</p>
<p>하지만, 코딩테스트에서는 대부분 <u>'최적의 해'</u>를 찾는 문제가 출제되기 때문에 그리디 알고리즘의 정당성을 고민하면서 문제 해결방안을
떠올려야 한다.</p>
<p>보통 코딩테스트에서 출제되는 그리디 알고리즘 유형의 문제는 창의력, 즉 문제를 풀기위한 최소한의 아이디어를 떠올릴 수 있는 능력을 요구한다.<p>
<p>그리디 알고리즘은 기준에 따라 좋은 것을 선택하는 알고리즘이므로 문제에서 <u>가장 큰 순서대로, 가장 작은 순서대로</u>와 같은 기준을</p>
<p>알게 모르게 제시해준다. 따라서 그리디 알고리즘 문제는 자주 정렬 알고리즘과 짝을 이루어 출제된다.</p>
<ol>
<li><a href="/greedy-theory/1.py">거스름돈</a><p>관련백준문제:https://www.acmicpc.net/problem/5585</p>
  <p>이 문제를 그리디 알고리즘으로 해결할 수 있는 이유는 <u>가지고 있는 동전 중에서 큰 단위가 항상 작은 단위의 배수이므로 
    <p>작은 단위의 동전들을 종합해 다른 해가 나올 수 없기 때문이다.</p></u></p>
  <p>예를 들어 800원을 거슬러 줘야 할 때 그리디 알고리즘으로는 500 + 100 + 100 + 100으로 나오지만, 최적의 해는 400+400이다.
    
<li><a href="/greedy-theory/2.py">큰 수의 법칙</a><p>관련백준문제:</p></li>
<li><a href="/greedy-theory/3.py">숫자 카드 게임</a><p>관련백준문제:</p></li>
    <li><a href="/greedy-theory/4.py">1이 될때까지</a> <p>관련백준문제:https://www.acmicpc.net/problem/1463</p></li>
</ol>
  
  ### 기출문제
  ----
  <ol>
  <li><a href="/greedy-sampletests/1.py">모험가 길드</a><p>관련백준문제:</p></li>
  <li><a href="/greedy-sampletests/2.py">곱하기 혹은 더하기</a><p>관련백준문제:</p></li>
  <li><a href="/greedy-sampletests/3.py">문자열 뒤집기</a><p>관련백준문제:</p></li>
  <li><a href="/greedy-sampletests/4.py">만들 수 없는 금액</a><p>관련백준문제:</p></li>
  <li><a href="/greedy-sampletests/5.py">볼링공 고르기</a><p>관련백준문제:</p></li>
  <li><a href="/greedy-sampletests/6.py">무지의 먹방 라이브</a><p>관련백준문제:</p></li>
  </ol>
  https://programmers.co.kr/learn/courses/30/lessons/42891?language=python3
  
# 2. 구현

## 아이디어를 코드를 바꾸는 구현


코딩테스트에서 구현이란 '머릿속에 있는 알고리즘을 소스코드로 바꾸는 과정' 이다.

어떤 문제를 풀든 간에 소스코드를 작성하는 과정은 필수이므로 구현 문제 유형은 모든 범위의 코딩테스트 문제 유형을 포함하는 개념이다.

흔히 개발할때 프로그래밍 언어의 문법에 능숙하고 코드작성속도(타자)가 빠른사람을 보고 '피지컬이 좋다'고 하는데, 구현 유형의 문제는 그런 의미에서 '피지컬'을 요구하는 문제이다.

이 책에서는 완전 탐색, 시뮬레이션 유형을 모두 '구현'유형으로 묶어서 다루고 있다.

`완전탐색` 은 모든 경우의 수를 주저없이 다 계산하는 해결 방법을 의미하고,

`시뮬레이션` 은 문제에서 제시한 알고리즘을 한 단계씩 차례대로 직접수행해야하는 문제 유형을 의미.



## 구현 시 고려해야할 메모리 제약 사항


파이썬에서 여러개의 변수를 사용할 때는 리스트를 이용한다. 파이썬에서 리스트를 이용할 때에 고려해야 할 사항이 있다.

바로 코딩 테스트의 메모리제한이다. 대체로 코딩테스트에서는 128~512 MB로 메모리를 제한하는데 알고리즘 문제 중 때로는 수백만개 이상의

데이터를 처리해야 하는 문제가 출제되곤 한다. 이럴 때는 메모리 제한을 염두에 두고 코딩해야 한다. 



## 채점환경


문제에서 요구하는 메모리 제한과 실행시간 제한은 코딩테스트를 출제하는 기관마다 ,문제마다 다르다.

일반적인 기업 코딩 테스트 환경에서는 파이썬으로 제출한 코드가 1초에 2,000만번 연산을 수행한다고 가정하면 크게 무리가 없다.

시간제한이 1초이고, 데이터의 개수가 100만개인 문제가 있다면 일반적으로 시간 복잡도 O(NlongN)이내의 알고리즘을 이용하여 문제를 풀어야한다.

실제로 N=1,000,000일 때 NlogN은 약 20,000,000이기 때문이다. 따라서 알고리즘 문제를 풀 때는 시간제한과 데이터의 개수를 먼저 확인한 후에 이 문제를 어느정도의 시간복잡도의 알고리즘으로 작성해야 풀 수 있을 것인지 예측할 수 있어야 한다.



## 구현 문제에 접근하는 방법


보통 구현 유형의 문제는 사소한 입력 조건 등을 문제에서 명시해주며 문제의 길이가 꽤 긴 편이다.

파이썬을 쓴다고 해서 항상 프로그램 동작 속도가 느린 것은 아니다. 자동 채점 방식을 이용하는 코딩테스트 환경에서는 점점 PyPy3를 지원하는 곳이 늘고 있다. 대부분 파이썬3보다 실행 속도가 더 빠르다. 특히 반복문이 많을 수록 PyPy3와 파이썬3의 속도가 차이가 나는데, 때론 C/C++에 견줄 만큼 빠르다.

따라서 코딩테스트 환경이 PyPy3를 지원하는지 확인하자.
  
  <ol>
<li><a href="">상하좌우</a><p>관련백준문제</p>
<li><a href="">시각</a><p>관련백준문제:https://www.acmicpc.net/problem/18312</p></li>
<li><a href="">왕실의 나이트</a><p>관련백준문제:https://www.acmicpc.net/problem/7562</p></li>
    <li><a href="">게임개발</a> <p>관련백준문제:https://www.acmicpc.net/problem/1516</p></li>
</ol>

# 3.DFS/BFS
  ### **탐색이란**
많은 양의 데이터 중에서 원하는 데이터를 찾는 과정을 의미한다.
프로그래밍에서는 그래프, 트리 등의 자료구조 안에서 탐색하는 문제를 다룬다
대표적인 탐색 알고리즘으로 DFS/BFS 를 제대로 이해하려면 기본 자료구조인 스택과 큐에 대한 이해가 전제 되어야 한다.

스택과 큐를 사용할 때는 삽입과 삭제 외에도 **오버플로와 언더플로**를 고민해야한다.
**오버플로**는 특정한 자료구조가 수용할 수 있는 데이터의 크기를 이미 찬 상태에서 삽입할 때 발생한다. 반대로 자료구조가 없을 때 삭제하려 하면 **언더플로**가 발생한다.

### 스택
스택은 FILO 또는 LIFO 즉 선입후출,후입선출 구조라고 한다.
**stack.append() stack.pop()** 과 같은 메소드를 구현 할 수 있다.

### 큐
큐는 선입선출 FIFO 구조라고 한다.
**from collections import deque** #collections 모듈에서 deque 자료구조 활용
**queue = deque()
queue.append() #맨 뒤에 갚 삽입
queue.popleft() #맨 앞쪽갚 삭제 및 return
queue.reverse() #역순으로**

dequeue는 스택과 큐의 장점을 모두 채택한 것인데, 데이터의 삽입과 삭제 속도가 리스트자료형에 비해 효율적이고 간단하다. 
대부분의 코딩테스트에서 collections 모듈과 같은 기본 라이브러리 사용을 허용한다.
dequeue 객체를 리스트 자료형으로 변경하고자 한다면 list 메서드를 이용하자. **list(dequeue)**

### 재귀함수
DFS 와 BFS를 구현하려면 재귀함수도 이해하고 있어야 한다. 

```python
def recursive_function:
	print('재귀함수를 호출합니다.')
    recursive_function()

recursive_function()
```
이 코드를 실행하면 '재귀 함수를 호출합니다' 라는 문자열을 무한히 출력한다.
물론 파이썬 인터프리터는 호출 횟수 제한이 있는데, 이 한계를 벗어나게 되면
recursive error가 뜬다.

재귀함수는 수학시간에 언급되는 프랙탈 구조와 흡사하다.

#### 재귀함수의 종료조건
```python
def recursive_function(i):
	if i == 100:
    	return 
    print(i,'번째 재귀 함수에서',i+1,'번째 재귀함수를 호출합니다.')
    recursive_function(i+1)
    print(i,'번째 재귀 함수를 종료합니다.')

recursive_function(1)
```
재귀함수의 수행은 스택 자료구조를 이용한다.
따라서 스택 자료구조를 활용해야하는 상당수 알고리즘은 재귀함수를 이용해서 간편하게 구현될수있다. DFS가 대표적인 예이다.

재귀함수를 이용하는 대표적 예제로는 팩토리얼 문제가 있다.
수학적으로 0!과 1!의 값은 1로 같다는 성질을 이용하여 팩토리얼 함수는 n이 1이하가 되었을 때 함수를 종료하는 재귀함수의 형태로 구현할 수 있다.

```python
#반복적으로 구현한 n!
def factorial_iterative(n):
	result = 1
    for i in range(1,n+1):
    	result *= i
    return result
#재귀적으로 구현한 n!
def factorial_recursive(n):
	if n <= 1:
    	return 1
    return n * factorial_recursive(n-1)
```
실행결과는 같지만 재귀함수가 재귀식(점화식)을 그대로 소스코드에 옮겼기 때문에 간결하다.

## 탐색 알고리즘 DFS/BFS
### DFS
DFS는 깊이 우선 탐색이라고도 부르며, 그래프에서 깊은 부분을 우선적으로탐색하는 알고리즘이다.
그래프는 **노드와 간선**으로 표현되며 이때 노드를 정점이라고도 말한다.
그래프 탐색이란 하나의 노드를 시작으로 다수의 노드를 방문하는 것을 말한다.

프로그래밍에서 그래프는 크게 2가지 방식으로 표현할 수 있는데 코딩테스트에서는 이 두 방식 모두 필요하다.
>인접 행렬 : 2차원배열로 그래프의 연결 관계를 표현하는 방식
>인접 리스트 : 리스트로 그래프의 연결 관계를 표현하는 방식

| |0|1  |2
-|-|-|-
0|0| 7 |5
1|7|0  |무한
2|5|무한|0
<left>
<img src="https://images.velog.io/images/grapefruitgreen/post/95ef8511-36d7-4f4d-b5e6-4d3fa0d71305/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-07-21%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%202.41.06.png" width =50%></img></left>



**인접 행렬방식은**
2차원 배열에 각 노드가 연결된 형태를 기록하는 방식이다.
위와 같이 연결된 그래프를 인접 행렬로 표현할 때 파이썬에서는 2차원 리스트로 구현할 수 있다.
연결이 되어있지 않은 노드끼리는 무한의 비용이라고 작성한다. 
실제 코드에서는 논리적으로 정답이 될수 없는 큰값중에서 999999999, 987654321 등의 값으로 초기화하는 경우가 많다.
이렇게 그래프를 인접행렬 방식으로 처리할 때는 다음과 같이 데이터를 초기화한다.
```python
INF = 999999999 #무한의 비용 선언
#2차원 리스트를 이용해 인접행렬 표현
graph= [
	[0,7,5],
    	[7,0,INF],
    	[5,INF,0],
    ]
print(graph)
```
>  [[0,7,5],[7,0,999999999],[5,999999999,0]]


**인접리스트 방식**에서는 
'연결리스트'라는 자료구조를 이용해 구현한다.
```python
#행(Row)이 3개인 2차원 리스트로 인접 리스트 표현
graph = [[] for _ in range(3)]
#노드 0에 연결된 노드정보 저장(노드,거리)
graph[0].append((1,7))
graph[0].append((2,5))
#노드 1에 연결된 노드정보저장(노드,거리)
graph[1].append((0,7))
graph[2].append((0,5))

print(graph)
```

> [[(1,7),(2,5)],[(0,7)],[(0,5)]]

이 두 방식은 어떤 차이가 있을까?

**메모리 측면에서** 보자면 <u>인접행렬방식은 모든 관계를 저장하므로 노드 개수가 많을수록 메모리가 불필요하게 낭비된다.</u>

반면에 <u>인접 리스트방식은 연결된 정보만을 저장하기 때문에 메모리를 효율적으로 사용한다.</u>

하지만 이와 같은 속성 때문에 인접리스트 방식은 인접행렬방식에 비해 특정한 두 노드가 연결되어있는지에 대한 정보를 얻는** 속도가 느리다.**
인접 리스트 방식에서는 연결된 데이터를 하나씩 확인해야 하기 때문이다.
그러므로 특정한 노드와 연결된 **모든 인접노드를 순회해야 하는 경우**, <u>인접 리스트 방식이 인접 행렬방식에 배해 메모리공간의 낭비가 적다.</u>

## DFS & BFS
**DFS는 스택자료구조를 이용하며 구체적인 동작 과정**은 다음과 같다.
1. 탐색 시작 노드를 스택에 삽입하고 방문 처리를 한다.
2. 스택의 최상단 노드에 방문하지 않은 인접 노드가 있으면 그 인접 노드를 **스택에 넣고 방문처리를 한다**. 방문하지 않은 인접 노드가 없으면 스택에서 최상단 노드를 꺼낸다.
3. 2번의 과정을 더이상 수행할 수 없을 때까지 반복한다. 

**노드1을 시작노드로 설정하여 DFS를 이용해 탐색을 진행하면 어떻게 될 까?
**


일반적으로 노드중에서 방문하지 않은 노드가 여러개 있으면 번호가 낮은 순서부터 처리한다.
DFS의 기능을 생각하면 순서와 상관없이 처리해도 되지만, 코딩테스트에서는 번호가 낮은 순서부터 처리하도록 명시하는 경우가 종종있다.
따라서 관행적으로 번호가 낮은 순서부터 처리하도록 구현하는 편이다.

**1.DFS**
![](https://blog.kakaocdn.net/dn/Bv5Mx/btqEeY5Gcf3/k3oaTXqflu0BHVBU7C2pQk/img.png)

**2.BFS**
![](https://blog.kakaocdn.net/dn/vkbVs/btqEgQMi4aI/VCoMxQODbVqBAxzVppVcCK/img.png)
**3. 비교**
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdpvYPB%2FbtqEiLJMF0L%2FzEzcxeZEHQZck5cT0IXOmk%2Fimg.gif)

### DFS 예제
```python
def dfs(graph, v,visited):
#현재 노드를 방문 처리
    visited[v] = True
    print(v,end=' ')
    #현재 노드와 연결된 다른 노드를 재귀적으로 방문
    for i in graph[v]:
    	if not visited[i]:
           dfs(graph, i, visited)
#각 노드가 연결된 정보를 리스트 자료형으로 표현(2차원 리스트)
graph = [ 
	[], 
	[2,3,8],
    	[1,7],
    	[1,4,5],
    	[3,5],
    	[3,4],
   	 [7],
    	[2,6,8],
    	[1,7]
    ]
#각 노드가 방문된 정보를 리스트 자료형으로 표현(1차원 리스트)
visited = [False] * 9
#정의된 DFS 함수 호출
dfs(graph,1,visited)
```
![](https://images.velog.io/images/grapefruitgreen/post/f93489a3-2322-43a2-a0b5-cbada2820357/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-07-21%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%2010.20.13.png)

### BFS
BFS 알고리즘은 '너비 우선 탐색' 이라는 의미를 가진다. 가까운 노드부터 탐색하는 알고리즘이다. DFS 는 최대한 멀리 있는 노드를 우선으로 탐색하는 방식으로 동작한다고 했는데, BFS는 그 반대이다.
BFS 구현에서는 선입선출 방식인 큐 자료구조를 이용하는 것이 정석이다.
인접한 노드를 반복적으로 큐에 넣도록 알고리즘을 작성.

#### 동작 방식
1. 탐색 시작 노드를 큐에 삽입하고 방문처리를 한다.
2. 큐에서 노드를 꺼내 해당 노드의 인접 노드 중에서 방문하지 않은 노드를 모두 큐에 삽입하고 방문 처리를 한다.
3. 2번의 과정을 더 이상 수행할수 없을 때까지 반복한다.

```python
from collections import deque
def bfs(graph, start, visited):
    queue = deque([start])
    visited[start] = True
    while queue:
    	v = queue.popleft()
        print(v,end=' ')
        for i in graph[v]:
            if not visited[i]:
            	queue.append(i)
                visited[i] = True
# 각 노드가 연결된 정보를 리스트 자료형으로 표현(2차원 리스트)
graph = [
	[], 
	[2,3,8],
    	[1,7],
    	[1,4,5],
    	[3,5],
    	[3,4],
   	 [7],
    	[2,6,8],
    	[1,7]
    ]
#각 노드가 방문된 정보를 리스트 자료형으로 표현(1차원 리스트)
visited = [False] * 9

#정의된 BFS 함수 호출
bfs(graph, 1, visited)
```

> 1 2 3 8 7 4 5 6

DFS BFS 의 구현 정리

|       |DFS |BFS|
|-------|----|---|
|동작 원리|스택 |큐  |
|구현방법|재귀함수 이용|큐 자료구조 이용|





