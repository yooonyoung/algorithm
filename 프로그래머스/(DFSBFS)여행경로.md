문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/43164

```
def solution(tickets):
    answer = []
    routes = {}
    for t in tickets:
        routes[t[0]] = routes.get(t[0], []) + [t[1]]
    for r in routes:
        routes[r].sort(reverse=True)
    current_list = ["ICN"]
    
    while current_list:
        current = current_list[-1]
        if current in routes and routes[current]:
            current_list.append(routes[current].pop())
        else:
            answer.append(current_list.pop())
            
    answer.reverse()
    return answer
```

