# Ex. No: 15A
# BINARY TREE - Creation of a Binary Tree with Three Nodes Using Python
## AIM:
To create a simple binary tree with one root node and two child nodes, and display the list of nodes.
## ALGORITHM:
```
1.Import the Node class from the binarytree module.
2.Input three elements from the user and store them in a list l.
3.Create the root node of the binary tree with the first element l[0].
4.Assign the second element l[1] as the left child of the root.
5.Assign the third element l[2] as the right child of the root
6.Print the list of nodes [root, root.left, root.right] to show the tree structure.
```

## PROGRAM:
```
from binarytree import Node
l=[]
for i in range(0,3):
    a=input()
    l.append(a)
root=Node(l[0])
root.left=Node(l[1])
root.right=Node(l[2])
print("List of nodes :",[root,root.left,root.right])
```
## OUTPUT

<img width="1176" height="235" alt="image" src="https://github.com/user-attachments/assets/6c4d00ac-6997-47f6-b6f5-bbff3f2f57bb" />

## RESULT
->The program successfully creates a binary tree with a root and two child nodes.

->The Node objects represent the nodes of the tree.

->The list displays the root and its left and right children.
