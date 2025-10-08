'''python3

class ListNode:
    def __init__(self,val=0,next=None):
        self.val = val
        self.next = next

class Solution:
    def deleteDuplicates(self,head):
        if not head:
            return head

        current = head

        while current.next:
            if current.val == current.next.val:
                current.next = current.next.next
            else:
                current = current.next
        return head

'''

感想
Arai60の問題を初めて解きました。ほとんどプログラミングしたことがなく、そもそも何をすることが要求されているのかもよくわかりませんでした。
どういう入力があって、自分はそれを処理するためにどういうコードを書く必要があって、どんな出力になったら正解なのかがよくわからなかったのです。
解答を見ると、classが定義されていて終わりですが、classを定義するだけでは普通は動かないと思います。内部ではどう処理されているのでしょうか。
そもそも何をしたら良いのかわからないので、解答を見ると、かろうじて理解はできました。ただ、基礎的な文法的知識の不足もありました。
まず、if not head の行がわからず調べたところ、None はFalseとみなされることを知りました。
while　のブロックがメインになっていて、次のノードの値が今いるノードの値と同じなら、次のノードを次の次のノードにする。そうでないなら、次のノードに進む。
それを繰り返しているというのは簡単でした。
アルゴリズム自体は難しくなく、非常に初歩的な問題なのだろうと思いました。ただ、文法やLeetcodeの使い方に怪しい点があるとわかりました。
読んで理解したら、その解答を思い出しつつ書き直しました。途中文法で詰まる点もあり、何度か書き直しました。それを繰り返すうちに、詰まることなく書けるようになりました。
