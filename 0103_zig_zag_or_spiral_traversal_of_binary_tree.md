# #103 - Zig-Zag or Spiral Traversal of Binary Tree

- **Striver's A2Z Topic:** 13.2: Medium Tree Problems
- **Date:** Fri, Oct 23, 2026
- **Blueprint Day:** Day 11

## Description & Notes

This Code is Similar to &nbsp;level Order Traversal.<br>
But its like one level must be Inverted. and one level must be in Same order. <br>
Dont Think Much.<br>
Take a count variable and increment it for Level by level.<br>
**For Even level Reverse the level array and add it in result array**. <br>
The Code Snippet:<br>
```cpp
int count=1;
        while(!q.empty()){
            int size=q.size();
            vector<int>level;
            for(int i=0;i<size;i++){
                    TreeNode* a=q.front();
                    if(a->left!=NULL)q.push(a->left);
                    if(a->right!=NULL)q.push(a->right);
                    level.push_back(a->val);
                    q.pop();
                }
            if(count%2==0){
                reverse(level.begin(),level.end());
            }
            res.push_back(level);
            count++;
            }
            return res;
```
