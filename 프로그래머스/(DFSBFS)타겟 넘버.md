문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/43165

```
def solution(numbers, target):
    answer = 0
    
    def calculate(numbers, target, idx=0):
        if idx < len(numbers):
            numbers[idx] *= 1
            calculate(numbers, target, idx+1)
            
            numbers[idx] *= -1
            calculate(numbers, target, idx+1)
            
        elif sum(numbers) == target:
            nonlocal answer
            answer += 1
            
    calculate(numbers, target)
            
    return answer
```

