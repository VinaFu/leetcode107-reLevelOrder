# leetcode107-reLevelOrder


方法一：偷懒！把顺序的结果倒过来- res【：：-1】

      class Solution:
        def levelOrderBottom(self, root: Optional[TreeNode]) -> List[List[int]]:

            res = []
            queue = deque([root])

            if not root:
                return []
            while queue:
                level = []
                for i in range(len(queue)):
                    cur = queue.popleft()
                    level.append(cur.val)
                    if cur.left:
                        queue.append(cur.left)
                    if cur.right:
                        queue.append(cur.right)
                res.append(level)

            return res[::-1]

方法二：???
