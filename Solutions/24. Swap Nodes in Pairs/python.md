```py

# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def swapPairs(self, head: Optional[ListNode]) -> Optional[ListNode]:
        if head and head.next:
            dummy = head
            head = head.next
            dummy.next = head.next
            head.next = dummy
            head.next.next = self.swapPairs(head.next.next)
        return head



```
