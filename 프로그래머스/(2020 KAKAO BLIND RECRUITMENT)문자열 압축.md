문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/60057

```
def solution(s):
    answer = []
    result = ""
    x = len(s)
    
    if x == 1:
        return x
        
    for i in range(1, (x//2)+1):
        count = 1
        temp = s[:i]
        for j in range(i, x, i):
            if s[j:j+i] == temp:
                count += 1
            else:
                if count == 1:
                    count = ""
                result += str(count) + temp
                temp = s[j:j+i]
                count = 1
                
        if count == 1:
            count = ""
        result += str(count) + temp
        answer.append(len(result))
        result = ""
        
    return min(answer)
```

