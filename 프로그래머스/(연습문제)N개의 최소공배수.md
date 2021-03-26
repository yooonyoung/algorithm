문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/12953

```
from math import gcd
def lcm(a,b):
    return a * b // gcd(a,b)
def solution(arr):
    while True:
        arr.append(lcm(arr.pop(0), arr.pop(0)))
        if len(arr) == 1:
            return arr[0]
```

