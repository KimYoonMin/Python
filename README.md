# Python
리스트 초기화
a = [1, 2, 3, 4, 5, 6, 7, 8, 9]
a = [0] * n

리스트 인덱싱과 슬라이싱
# 첫번째 원소 접근
a[0] 
# 뒤에서 첫번째 원소 접근
a[-1]
# 두번째 원소부터 네번째 원소까지
a[1 : 4]

리스트 컴프리헨션
# 0부터 9까지 선언
array = [i for i in range(10)]
# 0부터 19까지의 수에서 홀수만 포함하는 리스트
array = [i for i in range(20) if i % 2 == 1]
# 1부터 9까지 수들의 제곱값을 포함하는 리스트
array = [i * i for i in range(1, 10)]

2차원리스트 초기화
좋은 예 : array = [[0] * m for _ in range(n)]
나쁜 예 : array = [[0] * m] * n
