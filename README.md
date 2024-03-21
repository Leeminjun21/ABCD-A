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
