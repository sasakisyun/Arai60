"""python
class Solution:
    def hasCycle(self, head: Optional[ListNode]) -> bool:
        if head is None:
            return False

        visited = {}
        node = head

        while node.next:
            if node in visited:
                return True
            visited[node]=True
            node=node.next

        return False

"""

感想
・まずLeetCodeの使い方がわからなかったので、その確認になった。大学の授業では、コードを最初から最後まで書いたが、LeetCodeではclassの中身を書けば良いのだと分かった（AIに聞いた)。
・アルゴリズム自体は簡単だと思うが、自分では書けなかった。当たり前に思いつくようになりたい。
・コードを書いた経験に乏しく、文法も怪しかった。たとえばwhile node.next:という記述があるが、is not Noneと書かないといけないと思っていたこと。辞書[a]=bで辞書に値を追加できることを知らなかったことなど。
・コードを読んで理解して、一回書いてみたが小さいミスがあって書けなくて、また答えをみて一から書いたら書けた。その後何度か書いてみてスラスラ書けるようになったので、これで提出してみる。
