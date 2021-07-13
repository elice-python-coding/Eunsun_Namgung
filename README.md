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
  <p>예를 들어 800원을 거슬러 줘야 할 때 그리디 알고리즘으로는 500 + 100+100+100으로 나오지만, 최적의 해는 400+400이다.
    
<li><a href="/greedy-theory/2.py">큰 수의 법칙</a><p>관련백준문제:</p></li>
<li><a href="/greedy-theory/3.py">숫자 카드 게임</a><p>관련백준문제:</p></li>
    <li><a href="/greedy-theory/4.py">1이 될때까지</a> <p>관련백준문제:https://www.acmicpc.net/problem/1463</p></li>
</ol>

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


