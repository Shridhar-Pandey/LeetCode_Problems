``` java
import java.util.*;

class Solution {
    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
        List<Integer> finalList = new ArrayList<>();
        int i = 0;
        int j = 0;
        while (i < nums1.length && j < nums2.length) {
            if (nums1[i] <= nums2[j]) {
                finalList.add(nums1[i]);
                i++;
            } else {
                finalList.add(nums2[j]);
                j++;
            }
        }
        while (i < nums1.length) {
            finalList.add(nums1[i]);
            i++;
        }
        while (j < nums2.length) {
            finalList.add(nums2[j]);
            j++;
        }
        int size = finalList.size();
        return size % 2 == 0 ? (finalList.get(size / 2 - 1) + finalList.get(size / 2)) / 2.0 : finalList.get(size / 2);
    }
}
```
