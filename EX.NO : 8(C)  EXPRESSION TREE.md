
# EX.NO : 8(C)  EXPRESSION TREE 
 
# PROGRAM STATEMENT: 
 
To construct an expression tree from the given postfix expression. Generate the inorder and 
preorder traversal of the given expression tree below 
 
 ![image](https://github.com/user-attachments/assets/1eed4f2c-e6ce-4dc8-a66e-cfbde2a52556)


 
# ALGORITHM:   
 
1. Start the program. 
2. Define Node Class: Create a node class with attributes value, left, right, and next. Initialize the node with a constructor to set value and set left and right to NULL. 
3. Constructor: The parameterized constructor initializes the value and sets left and right pointers to NULL. The default constructor sets left and right pointers to NULL. 
4. Friend Classes: Declare stack and expression_tree as friend classes so they can access private members of the node class. 
5. End the program 
 
# PROGRAM:
```
class node {
public:
	char value;
	node* left;
	node* right;
	node* next = NULL;
	node(char c)
	{
		this->value = c;
		left = NULL;
		right = NULL;
	}
	node()
	{
		left = NULL;
		right = NULL;
	}
	friend class Stack;
	friend class expression_tree;
};
```

# output:

![image](https://github.com/user-attachments/assets/9055389b-7548-4147-a5a4-f5ddcd4c2e5c)

# RESULT: 
 
Thus, the C++ program to Generate the inorder and preorder traversal of the given expression tree below is created successfully. 


