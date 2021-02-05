문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/43163

```
def match(current, word):
    match_count = 0
    for c,w in zip(current, word):
        if c==w:
            match_count += 1
    if match_count == len(word)-1:
        return True
    else:
        return False
    
def solution(begin, target, words):
    if target not in words:
        return 0
    
    answer = 0
    visited = [0] * len(words)
    current_list = [begin]
    
    while current_list:
        current = current_list.pop()
        if current == target:
            return answer
        
        for i in range(len(words)):
            if not visited[i]:
                if match(current, words[i]):
                    visited[i] = 1
                    # print(current, words[i], visited)
                    current_list.append(words[i])
        answer += 1
```

