``` py
class Solution:
    def longestPalindrome(self, s: str) -> str:
        if s==s[::-1]:
            return s
        else:
            l=[]
            for i in range(len(s)):
                ls=""
                for j in range(i,len(s)):
                    ls=ls+s[j]
                    if ls==ls[::-1]:
                        l.append(ls)
            return max(l,key=len)
```
