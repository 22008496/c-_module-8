
# EX.NO : 8(A)  TREE REPRESENTATION AND TRAVERSALS 
 
# PROGRAM STATEMENT: 
 
 Write a C++ Function to perform Postorder traversal of the below given tree


 ![image](https://github.com/user-attachments/assets/3aa4ce6b-815d-4ef8-a329-987e7972344f)

 
# ALGORITHM:   
 
1. Start the program. 
2. Define Node: Create a Node structure with data and next pointer. 
3. Push: Insert a new node at the rear of the queue by updating the rear pointer. 
4. Pop: Remove the front node and update the front pointer, checking for underflow. 
5. Display: Print the queue from front to rear by traversing through all nodes. 
6. Display Front/Rear: Print the data of the front and rear nodes. 
7. Main: Perform push(), pop(), and display() operations on the queue. 
8. End the program. 
 
# PROGRAM:
```
void preorderTraversal(struct Node* node) {
  if (node == NULL)
    return;

  cout << node->data << "->";
  preorderTraversal(node->left);   // Correct order: Root → Left → Right
  preorderTraversal(node->right);
}
```
# output:

![image](https://github.com/user-attachments/assets/705335d5-eb17-4a50-8f2d-9b4982217dfc)

# RESULT: 
 
Thus, the C++ program to perform Postorder traversal of the below given tree is created successfully.


