# [리스트]
### 리스트 초기화
```python
a = [1, 2, 3, 4, 5, 6, 7, 8, 9]
a = [0] * n
```

### 리스트 인덱싱과 슬라이싱
```python
#첫번째 원소 접근
a[0] 
#뒤에서 첫번째 원소 접근
a[-1]
#두번째 원소부터 네번째 원소까지
a[1 : 4]
```

### 리스트 컴프리헨션
```python
#0부터 9까지 선언
array = [i for i in range(10)]
#0부터 19까지의 수에서 홀수만 포함하는 리스트
array = [i for i in range(20) if i % 2 == 1]
#1부터 9까지 수들의 제곱값을 포함하는 리스트
array = [i * i for i in range(1, 10)]
```
### 2차원리스트 초기화
```python
좋은 예 : array = [[0] * m for _ in range(n)]
나쁜 예 : array = [[0] * m] * n
```
### 리스트 관련 메서드
```python
a = [1, 4, 3]
#리스트에 원소 삽입
a.append(2)
#오름차순 정렬
a.sort()
#내림차순 정렬
a.sort(revers=True)
#리스트 원소 뒤집기
a.reverse()
#인덱스 2에 3추가
a.insert(2,3)
#특정 값인 데이터 갯수 세기
a.count(3)
#특정 값 데이터 삭제
a.remove(1)
```
### 리스트에서 특정값을 가지는 원소 모두제거
```python
a = [1,2,3,4,5,5,5]
remove_set = {3, 5}
result = [i for i in a if  i not in remove_Set]
```
# [문자열]
### 문자열연산
```python
print(a + " " + b)
print(a * 3)
print(a[2 : 4])
#문자열의 경우 특정 인덱스로 출력은 가능하나 변경은 불가능
가능   : print(a[2])
불가능 : a[2] = 'a'
```

# [튜플]
- 서로다른 성질의 데이터를 묶어 관리할때 사용
- 일반적으로 리스트와 사용은 비슷하나 메모리효율이 더 높음.
- 선언 후 변경이 불가능하기 때문에 키값으로 쓰임
```python
a = (1, 2, 3, 4, 5, 6, 7, 8, 9)
print(a[3])
print(a[1 :  4])
```
# [사전자료형]
- 키(Key)와 값(Value)의 쌍 데이터
- 변경 불가능한 자료형을 키로 사용
- 해시 테이블(Hash Table)을 이용하므로 데이터 조회 및 수정에 있어서 O(1)의 시간에 처리할 수 있음
```python
data = dict()
data['사과'] = 'Apple'
data['바나나'] = 'Banana'
data['코코넛'] = 'Coconut'

key_list = data.keys()
value_list = data.values()
# 각 키에 따른 값을 하나씩 출력
for key in key_list:
 print(data[key])
```

# [집합자료형]
### 초기화
```python
data = set([1,1,2,3,4,4,5])
data = {1,1,2,3,4,4,5} 
실행결과 : {1,2,3,4,5}
```
### 관련함수
```python
data = set([1,2,3])
# 새로운 원소 추가
data.add(4)
# 새로운 원소 여러개 추가
data.update([5,6])
# 특정한 값을 갖는 원소 삭제
data.remove(3)
```
# [사전 자료형과 집합 자료형의 특징]
- 리스트나 튜플은 수선가 있기 때문에 인덱싱으로 접근
- 사전 자료형과 집합 자료형은 순서가 없기 때문에 인덱싱값으로 접근 불가
  - 사전의 키(key) 혹은 집합의 원소(Element)를 통해 O(1)의 시간 복잡도로 조회

# [자주 사용되는 표준 입력 방법]
- input() 함수는 한줄의 문자열을 입력 받음
- map() 함수는 리스트의 모든 원소에 각각 특정한 함수를 적용할 때 사용
- 예시) 공백을 기준으로 구분된 데이터를 입력 받음\
`list(map(int, input().split()))`
- 예시) 공백을 기준으로 구분된 데이터의 개수가 많지 않다면, 단순히 다음과 같이 사용\
`a, b, c = map(int, input().split())`
### 빠르게 입력 받기
```python
import sys
data = sys.stdin.readline().rstrip()
print(data)
```
### 출력을 위한 전형적인 소스코드
```python
a=1
b=2
print(a, b) # print의 경우 기본적으로 줄바꿈
print(7, end=" " ) # end를 써서 줄바꿈을 없앰
print(8, end=" ")

answer = 7
print("정답은 " + str(answer) + "입니다.")
```
### f-string 예제
- 파이썬 3.6부터 사용 가능하며, 문자열 앞에 접두사 'f'를 붙여 사용
-  중괄호 안에 변수명을 기입하여 간단한 문자열과 정수를 함께 넣을 수 있음
```python
answer = 7
print(f"정답은 {answer}입니다.")
```
# [조건문]
### 조건문 간소화
```python
score = 85
result = "Sucess" if score >= 80 else  "Fail"
```
### 조건문 내에서의 부등식
```python
x = 15
if 0<x<20:
 print("x는 0이상 20미만의 수입니다.")
```
### 특정리스트에 존재여부
```python
if i in list:
  print("리스트에 존재합니다.")
else:
  print("리스트에 존재하지 않습니다.")
```
# [함수]
### 선언
```python
def 함수명(매개변수1, 매개변수2):
  실행코드
  return 반환값
```
### global
```python
a = 0
def func():
  global a
  a += 1

for _ in range(10);
  func()

print(a)
```
### 여러개의 반환 값
```python
def operator(a, b):
  add_var = a+b
  subtract_var = a-b
  multiply_var = a*b
  divide_var = a/b
  return add_var, subtract_var, multiply_var, divide_var

a, b, c, d = operator(7 , 3)
```
### 람다 표현식
- 특정한 기능을 수행하는 함수를 한줄에 작성
```python
print((lambda a, b: a + b)(3, 7))

#여러개의 리스트에 적용
list1 = [1, 2, 3, 4, 5]
list2 = [6, 7, 8, 9, 10]
result = map(lambda a, b: a+b, list1, list2)
print(list(result))
```
### 자주 사용되는 내장 함수
```python
# sum()
result = sum([1, 2, 3, 4, 5])
# min(), max()
min_result = min(7, 3, 5, 2)
max_result = max(7, 3, 5, 2)
# eval()
result = eval=("(3+5)*7")

# sorted()
result = sorted([9, 1, 8, 5, 4])
reverse_result = sorted([9, 1, 8, 5, 4], reverse=True)
 # sorted() with key
array = [('홍길동', 35), ('이순신', 75), ('아무개', 50)]
result = sorted(array, key=lambda x: x[1], reverse=True)
```
# [순열과 조합]
- 순열: 서로다른 n개에서 서로 다른 r개를 선택하여 일렬로 나열
```python
from itertools import permutations
data = ['A', 'B', 'C']
result = list(permutations(data, 3))
```
- 조합 : 서로다른 n개에서 순서에 상관없이 r개를 선택하여 일렬로 나열
```python
from itertools import combinations
data = ['A', 'B', 'C']
result = list(combinations(data, 3))
```
### 중복 순열과 중복 조합
```python
from itertools import product
data = ['A', 'B', 'C']
result = list(product(data, repeat=2))

from itertools import combinations_with_replacement
data = ['A', 'B', 'C']
result = list(combinations_with_replacement(data, 2))
```
# [Counter]
- 리스트와 같은 반복 가능한(iterable) 객체가 주어졌을때 ***내부의 원소가 몇 변씩 등작했는지*** 알려줌
```python
from collections import Counter
counter = Counter(['red','blue','red','green','blue','blue'])

print(counter['blue'])
print(dict(counter)) #사전 자료형으로 반환
```
# [최대 공약수와 최소 공배수]
- 최대 공약수를 구할때는 math 라이브러리의 gcd() 함수이용
```python
import math
# 최소 공배수(LCM)를 구하는 함수
def lcm(a, b):
  return a*b // math.gcd(a, b)

a = 21
b = 14
print(math.gcd(21, 14))
print(lcm(21, 14))
```
