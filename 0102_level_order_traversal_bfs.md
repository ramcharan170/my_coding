# #102 - Level Order Traversal / BFS

- **Striver's A2Z Topic:** 13.1: Tree Traversals
- **Date:** Fri, Oct 23, 2026
- **Blueprint Day:** Day 11

## Description & Notes

This problem Uses Queue. Remember that.<br>
First we insert root in the queue. <br>
The Logic To do here is: <br>
1. For Each Element in the level we iterate through and insert the left and right in the Queue. And then in the end we just pop the Element and add it into the **level** array.

2.After the size loop ends add the level array to the result array. <br>

3. Do this Until the Queue is empty.
**Code:**<br>


```cpp
vector<vector<int>> levelOrder(TreeNode* root) {
        vector<vector<int>>res;
        queue<TreeNode*>q;
        if(root==NULL)return res;
        q.push(root);
        while(!q.empty()){
            vector<int>level;
            int size=q.size();
            for(int i=0;i<size;i++){
                TreeNode* a=q.front();
                if(a->left!=NULL) q.push(a->left);
                if(a->right!=NULL)q.push(a->right);
                level.push_back(a->val);
                q.pop();
            }
            res.push_back(level);
        }
        return res;
    }
```
Check the Code carefully.<br>
