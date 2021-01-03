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
