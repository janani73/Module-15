# Ex. No: 15C - Expression Tree Traversal Using Python binarytree Module

## AIM:
To create a binary tree representing an arithmetic expression and demonstrate inorder and postorder traversals.
## ALGORITHM:
```
1.Import build and Node from the binarytree module.
2.Prepare a list x representing a binary tree in level-order (nodes of an expression tree).
3.Build the binary tree using build(x).
4.Perform traversals:
      ->Inorder traversal: Visit left subtree → root → right subtree.
      ->Postorder traversal: Visit left subtree → right subtree → root.
5.Print the result of both traversals.
```
## PROGRAM:

```
from binarytree import build,Node
x=['*','+','-',9,3,8,4]
t=build(x)
print(t.inorder)
print(t.postorder)
```

## OUTPUT:

<img width="1173" height="227" alt="image" src="https://github.com/user-attachments/assets/2bfbd8c6-5a58-43e4-aac6-90fceaa4a476" />

## RESULT:
->The program constructs a binary tree from the given list.

->inorder traversal prints the expression in standard infix order.

->postorder traversal prints the expression in postfix order.
