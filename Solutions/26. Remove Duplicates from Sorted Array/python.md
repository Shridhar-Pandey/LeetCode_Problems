```py
public class Solution {
    public int removeDuplicates(int[] nums) {
        if (nums.length == 0) {
            return 0;
        }

        int maxValue = nums[0];
        int k = 1;
        for (int i = 1; i < nums.length; i++) {
            if (nums[i] > maxValue) {
                maxValue = nums[i];
                nums[k] = maxValue;
                k++;
            }
        }
        return k;
    }
}



```
