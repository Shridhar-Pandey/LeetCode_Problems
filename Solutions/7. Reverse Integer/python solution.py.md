``` py
class Solution:
	def reverse(self, x: int) -> int:
		sign = 1
		if x < 0:
			sign = -1
			x = -x
		res = 0
		while x:
			res = res*10+x % 10
			x //= 10
		return 0 if res > (1 << 31) else res*sign

```
