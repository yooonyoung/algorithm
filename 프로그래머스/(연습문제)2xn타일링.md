문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/12900

```
def solution(n):
    answer = 0
    dp = [0] * 60001
    for i in range(n+1):
        if i == 0 or i == 1:
            dp[i] = 1
        else:
            dp[i] = (dp[i-1] + dp[i-2]) % 1000000007
    return dp[n] 
```

