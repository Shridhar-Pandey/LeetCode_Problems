``` py

class Solution:
    def isValid(self, s: str) -> bool:
        dicts = {')':'(', ']':'[', '}':'{'}
        stack = []
        for i in s:
            if i in dicts:
                if stack!=[] and stack.pop() == dicts[i]:
                    continue
                else:
                    return False
            else:
                stack.append(i)
        if stack:
            return False
        else:
            return True



```
