# ステップ１

## １回目

### コード
書けなかった。

### 考えたこと、コメント
- valueが同じnodeが連続していたら取り除けばいいので、whileを使ってvalueが等しくないnodeが出てくるまで見ればいいのではないか。
- valueが等しくないnodeが出てきたら、83.Remove Duplicates でやったように、node.next = (valueが等しいnodeたちの次のnode)とすれば良いのではないか
- 先頭からvalueが等しいnodeが続いていたら困ると思った。その場合、node.nextを違うnodeにするという方法でnodeを取り除けないのではないか。

### 感想


## 2回目

### コード（途中で断念）
```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def deleteDuplicates(self, head: Optional[ListNode]) -> Optional[ListNode]:
        dummy = ListNode(0,head)
        node = head
        pred = dummy
        while node:
            if node.next and node.val == node.next.val:
                while node.val == node.next.val:
                    node = node.next
                #ここで、node.val != node.next.valになってる
                pred = 
            else:
                pred.next = node
```
### 考えたこと、コメント
- いくつか解答例を読んでみるも、あまり理解できず、Geminiにコードを書かせて質問して理解した。
- headの前に余分なnodeを追加することで、私の困っていた点が解消されていた。
- Geminiはheadをそのまま変数名としてコードを書いていたが、headは最初のノードを表すのにそれは変ではないかと思った。
- 途中で手が動かなくなったのは、理解不足が原因だ。連結リストを更新していてる場所と、単に連結リストの上を走査しているだけの場所の区別がついていない。
- 再び解答を読み直し、3回目を行う。

## 3~5回目

### コード
```python
class Solution:
    def deleteDuplicates(self, head: Optional[ListNode]) -> Optional[ListNode]:
        if not head or not head.next :
            return head
        dummy = ListNode(0,head)
        node = head
        pred = dummy
        while node:
            if node.next and node.val == node.next.val:
                while node.next and node.val == node.next.val: #ここでnode.nextを入れ忘れた
                    node = node.next
                pred.next = node.next
            else:
                pred = pred.next
            node = node.next
        return dummy.next

```
### 考えたこと、コメント
- コードを理解したので再度取り組んだ
- 上でコメントした点でnode.nextの条件に言及せずエラーになった
- 4回目はタイプミスをした
- 5回目でacceptされた

## 6回目
OK

## 7回目
OK

## ステップ１を通しての感想
- この問題は解けなかっただけでなく、コードを読んでもすぐには理解できなかった。
- 理解したし書けるようにもなったが、なんだかこのコードになる必然性を感じない。続けて書いているので覚えているから書けてしまっている面もあるかも知れない。
- これまでのPRではコードと簡単な感想しか書いていなかったのだが、もっと詳細に過程を書くように言われたので書くようにした。これで良いのだろうか。






