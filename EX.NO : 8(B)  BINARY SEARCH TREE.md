# EX.NO : 8(B)  BINARY SEARCH TREE 
 
# PROGRAM STATEMENT: 

Write a C++ Function that checks whether a tree is a Binary Search Tree or not.

 
 
# ALGORITHM:   
 
1. Start the program. 
2. Define Function: Create a function convertBST that takes the root of the BST, an InOrderArray, and an index i as input. 
3. Traverse Left Subtree: Recursively call convertBST on the left child of the current node. 
4. Assign Data: Assign the value from InOrderArray[i] to the current node’s data, then increment i. 
5. Traverse Right Subtree: Recursively call convertBST on the right child of the current node. 
6. End the program.

# Program:
```
bool isBST(node *root)
{
   node *prev = NULL;
   return isBSTUtil(root, prev);
}
```

# output:

![image](https://github.com/user-attachments/assets/9b4a3acc-7ed9-4179-a0a4-1d12608dc04f)

# Result:
thus the C++ Function that checks whether a tree is a Binary Search Tree or not is executed successfully.
