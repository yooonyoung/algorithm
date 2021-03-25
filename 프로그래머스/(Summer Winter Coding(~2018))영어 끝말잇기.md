문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/12981

```
def solution(n, words):
    answer = [0,0]
    said = [words[0]]
    num = 0
    for i in range(len(words)):
        num %= n
        if i >= 1:
            if words[i] in said or words[i-1][-1] != words[i][0]:
                answer = [num+1, i//n+1]
                break
        num += 1
        said.append(words[i])
    return answer
```

