문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/43162

```
def solution(n, computers):
    answer = 0
    visited = [0 for i in range(n)]
    for com in range(n):
        if visited[com] == 0:
            BFS(n, computers, com, visited)
            answer += 1
    return answer

def BFS(n, computers, com, visited):
    visited[com] = 1
    queue = []
    queue.append(com)
    while queue:
        current = queue.pop(0)
        visited[current] = 1
        for i in range(n):
            if com != i and computers[current][i] == 1:
                if visited[i] == 0:
                    queue.append(i)
```

