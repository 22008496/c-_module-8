
# EX.NO : 8(D)  AVL TREE 
 
# PROGRAM STATEMENT: 
 
To write a C++ code to perform LL & RR rotation in an AVL Tree while inserting elements. 
 
# ALGORITHM:   
 
1. Start the program. 
2. Insert Node: Define the function insert() to insert a new key in the AVL tree. If the tree is empty, create a new node with the given key. 
3. Normal BST Insertion: Traverse the tree recursively and insert the node at the appropriate position based on the comparison of the key with the current node's key. 
4. Update Height: After insertion, update the height of the ancestor node based on the maximum height between the left and right child. 
5. Check Balance Factor: Calculate the balance factor of the current node to check if it has become unbalanced. If unbalanced, handle it with appropriate rotations (left or right). 
6. End the program. 
 
# PROGRAM:
```
Node* insert(Node* node, int key)
{
    // 1. Perform the normal BST insertion
    if (node == nullptr)
        return new Node{key, nullptr, nullptr, 1};

    if (key < node->key)
        node->left = insert(node->left, key);
    else if (key > node->key)
        node->right = insert(node->right, key);
    else
        return node; // Duplicate keys not allowed

    // 2. Update height of this ancestor node
    node->height = 1 + max(height(node->left), height(node->right));

    // 3. Get the balance factor
    int balance = getBalance(node);

    // 4. Balance the tree

    // Left Left Case
    if (balance > 1 && key < node->left->key)
        return rightRotate(node);

    // Right Right Case
    if (balance < -1 && key > node->right->key)
        return leftRotate(node);

    // Left Right Case
    if (balance > 1 && key > node->left->key) {
        node->left = leftRotate(node->left);
        return rightRotate(node);
    }

    // Right Left Case
    if (balance < -1 && key < node->right->key) {
        node->right = rightRotate(node->right);
        return leftRotate(node);
    }

    return node;
}
```

# output:

![image](https://github.com/user-attachments/assets/a1fe721e-dc81-4574-b66b-8ef8e2e19e88)

# RESULT: 
 
Thus, the C++ program to perform LL & RR rotation in an AVL Tree while inserting elements is created successfully.
