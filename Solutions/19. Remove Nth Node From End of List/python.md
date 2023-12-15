``` py

class Solution:
    def removeNthFromEnd(self, head: ListNode, n: int) -> ListNode:
        dummy = ListNode(0)
        dummy.next = head
        length = 0
        curr = head
        while curr:
            length += 1
            curr = curr.next
        curr = dummy
        for i in range(length - n):
            curr = curr.next
        curr.next = curr.next.next
        return dummy.next



```
