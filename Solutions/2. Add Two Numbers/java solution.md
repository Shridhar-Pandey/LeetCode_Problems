``` java
public class Solution {
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
        ListNode root = new ListNode(0);
        ListNode result = root;
        int excess = 0;
        while (l1 != null || l2 != null || excess != 0) {
            if (l1 != null) {
                excess += l1.val;
                l1 = l1.next;
            }
            if (l2 != null) {
                excess += l2.val;
                l2 = l2.next;
            }
            result.next = new ListNode(excess % 10);
            result = result.next;
            excess = excess / 10;
        }
        return root.next;
    }
}
```
