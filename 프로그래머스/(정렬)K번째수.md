문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/42748

```
def solution(array, commands):
    answer = []
    for c in commands:
        slice = array[c[0]-1:c[1]]
        slice.sort()
        answer.append(slice[c[2]-1])
    return answer
```

