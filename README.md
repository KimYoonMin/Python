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
