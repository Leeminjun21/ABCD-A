# ABCD-A 03.21

##  람다 함수 이용해서 10의 제곱 구하는 코드

```언어
x = lambda a : a * a
print(x(10))
```

##  QUIZ
numbers 리스트의 항목 중 짝수인 것만 필터링해서 result에 저장한 후 출력하는 코드

```언어
numbers = [111, 26, 37, 48]

result = list(filter(lambda x: x % 2 == 0, numbers))

print(result)
```


# 04.04
```언어
#quiz 1
def print_star_pattern():
    a = '★'
    for i in range(3):
        for j in range(4):
            print(a, end=' ')
        print()

print_star_pattern()
```

```언어
#quiz 2
def print_star_pattern():
    """
    별 패턴을 출력하는 함수
    """
    a = '★'
    for i in range(3):
        print((a + ' ') * 4)

# 함수 호출
print_star_pattern()
```

```언어
#quiz 3
def print_pattern(character, num_rows, num_columns):
    """
    주어진 문자와 반복 횟수에 따라 패턴을 출력하는 함수

    Args:
    - character (str): 출력할 문자
    - num_rows (int): 반복할 행의 개수
    - num_columns (int): 반복할 열의 개수
    """
    # 지정된 행과 열 개수만큼 패턴 출력
    for i in range(num_rows):
        for j in range(num_columns):
            print(character, end=' ')
        print()

# 함수 호출
print_pattern('★', 4, 3)
```

```언어
#quiz 4
def print_stars(num_stars, num_rows):
    """
    주어진 별의 개수와 반복 횟수에 따라 별을 출력하는 함수

    Args:
    - num_stars (int): 출력할 별의 개수
    - num_rows (int): 반복 횟수
    """
    star = '★'  # 별을 ★로 변경
    # 가로로 연결된 별을 num_rows 번 반복하여 출력
    for _ in range(num_rows):
        print(star * num_stars)

# 함수 호출
print_stars(4, 3)
```

```언어
#quiz 5 1.사용자로부터 입력 받는 방법:
import math

def calculate_cylinder_volume_from_user_input():
    """
    사용자로부터 반지름과 높이를 입력받아 원기둥의 부피를 계산하고 출력하는 함수
    """
    while True:
        r = input("반지름을 입력하세요 (종료하려면 'q'를 입력하세요): ")
        if r == 'q':
            break
        r = float(r)
        h = float(input("높이를 입력하세요: "))
        volume = math.pi * r ** 2 * h
        print("원기둥의 부피는:", volume)

# 함수 호출
calculate_cylinder_volume_from_user_input()
```

```언어
#quiz 5 2.변수에 값을 직접 지정하는 방법:
import math

def calculate_cylinder_volume(radius, height):
    """
    주어진 반지름과 높이를 사용하여 원기둥의 부피를 계산하고 출력하는 함수

    Args:
    - radius (float): 원기둥의 반지름
    - height (float): 원기둥의 높이
    """
    volume = math.pi * radius ** 2 * height
    print("원기둥의 부피는:", volume)

# 함수 호출
calculate_cylinder_volume(5, 10)
```

```언어
#quiz 6-1
import datetime

def print_current_datetime():
    """
    현재 날짜와 시간을 출력하는 함수
    """
    x = datetime.datetime.now()
    print(x)

# 함수 호출
print_current_datetime()
```

```언어
#quiz 6-2
import datetime

def print_current_time():
    """
    현재 시간을 출력하고 사용자로부터 프로그램 종료 여부를 확인하는 함수
    """
    while True:
        # 현재 시간을 가져옵니다.
        current_time = datetime.datetime.now()

        # 년, 월, 일, 시간, 분, 초를 각각 변수에 저장합니다.
        year = current_time.year
        month = current_time.month
        day = current_time.day
        hour = current_time.hour
        minute = current_time.minute
        second = current_time.second

        # 현재 날짜의 요일을 가져옵니다.
        weekday = current_time.strftime("%A")

        # 시간을 출력합니다.
        print("현재 시간:")
        print(f"년: {year}")
        print(f"월: {month}")
        print(f"일: {day}")
        print(f"시간: {hour}")
        print(f"분: {minute}")
        print(f"초: {second}")
        print(f"요일: {weekday}")

        # 사용자가 프로그램을 종료하고 싶으면 'q'를 입력합니다.
        user_input = input("프로그램을 종료하려면 'q'를 입력하세요: ")
        if user_input.lower() == 'q':
            print("프로그램을 종료합니다.")
            break

# 함수 호출
print_current_time()
```

```언어
#quiz 7
def print_tall_students_height(student_heights):
    """
    주어진 학생들의 키 리스트에서 170보다 큰 키를 가진 학생들의 키를 출력하는 함수

    Args:
    - student_heights (list): 학생들의 키가 포함된 리스트
    """
    # 학생들의 키를 순회하면서 170보다 큰 경우 출력
    for height in student_heights:
        # 키가 170보다 작으면 다음 학생의 키를 확인
        if height <= 170:
            continue
        # 키가 170보다 큰 경우에만 출력
        print(f"키가 170보다 큰 학생의 키: {height}")

# 함수 호출
print_tall_students_height(student_heights)
```



