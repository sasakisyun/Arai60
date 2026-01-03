```Python

# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def deleteDuplicates(self, head: Optional[ListNode]) -> Optional[ListNode]:
        if not head:
            return None
        temp = head
        while temp:
            if temp.next and temp.val == temp.next.val:
                temp.next = temp.next.next
            else:
                temp = temp.next
        return head

```

感想
まだコードを書くことに慣れておらず、同じものが出てきたら取り除くという簡単な操作でも一苦労だ。ポインターを動かしていって、同じものが出てきたら取り除けばいいのだろう、でも取り除くってどうやるんだろうと思って止まってしまった。
解答を見て、今見てるnodeのvalueと次のnodeのvalueが一緒なら、今のnodeから出てる矢印の先端を次のnodeから外して、次の次のnodeに付け替えればいいんだな、と把握して、手を動かしてみたところ完成できた。時間はなくても、１日１問は解くようにしたい。
