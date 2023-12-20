``` py
class Solution:
    def generateParenthesis(self, n: int) -> List[str]:
        if n==1:
            return ["()"]
        ans ={"()"}
        for i in range(n-1):
            x = set()
            for elem in ans:
                for c in range(len(elem)):
                    x.add(elem[:c]+"()"+elem[c:])
            ans = x
        return ans


```
