문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/42747/

```
def solution(citations):
    citations.sort(reverse=True)
    print(citations)
    answer = len(citations)
    while True:
        count = 0
        for c in citations:
            if c >= answer:
                count += 1
            if count >= answer:
                return answer
        answer -= 1

```

