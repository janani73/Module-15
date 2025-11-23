# Ex. No: 15B - Deletion of a Node from a Binary Search Tree (BST) in Python

## AIM:
To demonstrate how to delete a node from a Binary Search Tree while maintaining the BST property, and display the tree before and after deletion.
## ALGORITHM:
```
1.Define a helper function _build_bst_from_sorted_values(sorted_values) to build a balanced BST from a sorted list:
        ->If the list is empty, return None.
        ->Find the middle element of the list to create the root node.
        ->Recursively build the left subtree from elements before the middle.
        ->Recursively build the right subtree from elements after the middle.
        ->Return the root node.
2.Define del_BST(val) function to delete a value from the BST:
        ->If val exists in the global list x, remove it.
        ->Rebuild a balanced BST from the updated sorted list.
        ->Return the updated BST.
3.Define display(T) function to traverse the BST and print its values in order:
         ->Iterate through T.values (inorder traversal).
4.Initialize the list of BST elements x=[3,1,4,2].
5.Build and display the BST before deletion using _build_bst_from_sorted_values.
6.Input the value s to delete from the BST.
7.Call del_BST(s) to delete the node and rebuild the BST.
8.Display the updated BST.
```
## PYTHON PROGRAM

```
from binarytree import Node
def _build_bst_from_sorted_values(sorted_values):
    if len(sorted_values) == 0:
        return None
    mid_index = len(sorted_values) // 2
    root = Node(sorted_values[mid_index])
    root.left = _build_bst_from_sorted_values(sorted_values[:mid_index])
    root.right = _build_bst_from_sorted_values(sorted_values[mid_index + 1 :])  
    return (root)
def del_BST(val):
  global x
  if val in x:
    x.remove(val)
    tree=_build_bst_from_sorted_values(sorted(x))
  else:
    return False
  return tree
def display(T):
  for i in T.values:
    print(i,"-->",end="")
x=[3,1,4,2]
print("BST before deletion: ")
t=_build_bst_from_sorted_values(sorted(x))
display(t)
s=int(input())
print("\nBST after deletion:")
t1=del_BST(s)
display(t1)
```

## OUTPUT
<img width="1177" height="262" alt="image" src="https://github.com/user-attachments/assets/f0f974d8-a871-4a7c-b94b-315b0c25e444" />

## RESULT
->The program successfully deletes the specified node from the BST.

->The BST remains balanced and retains its properties.

->The inorder traversal before and after deletion shows the updated tree structure.
