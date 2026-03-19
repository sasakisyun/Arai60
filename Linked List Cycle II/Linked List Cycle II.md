```python

# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def detectCycle(self, head: Optional[ListNode]) -> Optional[ListNode]:
        slow = head
        fast = head
        while fast and fast.next:
            slow = slow.next
            fast = fast.next.next
            if slow == fast:
                slow = head
                while slow != fast:
                    slow = slow.next
                    fast = fast.next
                return slow
        return None
```

感想など
・アルゴリズムについての知識が全然ないので、このアルゴリズムも初見だった。あまり直感的に受け入れられないが、とりあえずそういうものだと思って覚えるしかないと思った。
・解答を読んで、while fast and fast.nextの部分が単にfastではダメなのかと思って試したら、Noneのnextがないということでエラーになった。
・前回から期間が少し開いてしまったが、習慣化して時間を見つけて取り組みたい。
・大学生なので、春休みに集中的にLeetCodeをやり、OdaさんのブログやDiscordで紹介されていた本も読みたいと思う。期限を設けて集中的に取り組まないと、いつまでもダラダラ時間をかけてしまいそう。
        




