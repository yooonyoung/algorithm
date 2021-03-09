문제 링크 : https://programmers.co.kr/learn/courses/30/lessons/60058

```
def solution(p):
    if p == "":
        return ""
    return func(p)

def func(p):
    if p == "":
        return ""
    left, right = 0,0
    u,v = "",""
    for i in range(len(p)):
        if p[i] == "(":
            left += 1
        else:
            right += 1
        if left == right:
            u = p[:i+1]
            v = p[i+1:]
            break
    if isRightBracket(u):
        u += func(v)
        return u
    else:
        string = "(" + func(v) + ")"
        u = u[1:len(u)-1]
        u = reverseBracket(u)
        string += u
        return string
        
def isRightBracket(p):
    stack = []
    for c in p:
        if len(stack) == 0:
            if c == "(":
                stack.append(c)
            else:
                return False
        else:
            if c == "(":
                stack.append(c)
            else:
                stack.pop()
    if len(stack) == 0:
        return True
    else:
        return False

def reverseBracket(p):
    fixed_p = ""
    for s in p:
        if s == "(":
            fixed_p += ")"
        else:
            fixed_p += "("
    return fixed_p
```

