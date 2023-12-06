``` py

class Solution:
    def myAtoi(self, s: str) -> int:
        s = s.strip()
        if not s:
            return 0
        sign = -1 if s[0] == '-' else 1
        if s[0] in ['-', '+']:
            s = s[1:]
        res = 0
        for c in s:
            if not c.isdigit():
                break
            res = res * 10 + int(c)
        res *= sign
        return max(-2**31, min(res, 2**31 - 1))

```
