``` py

class Solution:
    def lengthOfLongestSubstring(self, s: str) -> int:
        if len(s)==0:
            return 0
        r=s[0]
        m,i,k= 1,1,1
        while i<len(s):
            if s[i] in r:
                if len(r)>m:
                    m=len(r)
                if k<len(s):                    
                    i=k
                    k=k+1
                r=s[i]
                i=i+1
            else:
                r=r+s[i]
                i=i+1
        return max(m,len(r))
```
