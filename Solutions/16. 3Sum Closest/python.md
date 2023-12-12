``` py
class Solution:
    def threeSumClosest(self, nums: List[int], target: int) -> int:
        nums.sort()
        n = len(nums)
        sum = nums[0] + nums[1] + nums[2]
        for i in range(n-2):
            j = i + 1
            k = n - 1
            while j < k:
                temp = nums[i] + nums[j] + nums[k]
                if abs(temp - target) < abs(sum - target):
                    sum = temp
                if temp > target:
                    k -= 1
                elif temp < target:
                    j += 1
                else:
                    return target
        return sum




```
