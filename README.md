# Leetcode-145.-Binary-Tree-Postorder-Traversal
# Description
Given the root of a binary tree, return the postorder traversal of its nodes' values.

Postorder traversal is a tree traversal algorithm that visits the nodes of a binary tree in the order: left subtree, right subtree, then the root node

Example:

<img width="300" height="168" alt="image" src="https://github.com/user-attachments/assets/acc3b373-5b12-4d50-a3b4-4902f3f059e3" />

# Algorithm
1. Start from the root node.
2. Traverse the left subtree recursively.
3. Traverse the right subtree recursively.
4. Process the current node (e.g., print or store its value).
5. Repeat for all nodes until the whole tree is visited.

# Code 
class Solution:
    def postorderTraversal(self, root: Optional[TreeNode]) -> List[int]:
        res=[]
        
        def postorder(root):
            if root is None:
                return None
            postorder(root.left)
            postorder(root.right)
            res.append(root.val)
        postorder(root)
        return res
# Complexity
⏱️ Time Complexity – O(n)

Each node is visited exactly once.

So for n nodes, total time = O(n).
