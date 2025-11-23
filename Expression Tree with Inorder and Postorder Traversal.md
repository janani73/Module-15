# Ex. No: 15E - Insertion into a Binary Search Tree (BST) Using Python

## AIM:
To demonstrate insertion of a new element into a Binary Search Tree while maintaining the BST property and display the tree before and after insertion.
## ALGORITHM:
```
1.Define a helper function _build_bst_from_sorted_values(sorted_values) to create a balanced BST from a sorted list:
      ->If the list is empty, return None.
      ->Find the middle element to create the root node.
      ->Recursively create the left subtree from elements before the middle.
      ->Recursively create the right subtree from elements after the middle.
      ->Return the root node.
2.Initialize a list x with BST elements [8, 5, 14, 1, 7, 10, 20].
3.Sort the list and build the BST using _build_bst_from_sorted_values.
4.Display the BST elements in order using root.values.
5.Input a new element to insert.
6.Append the new element to the list x.
7.Sort the updated list and rebuild the BST.
8.Display the updated BST elements.
```
## PROGRAM:

```
from binarytree import build,Node
def _build_bst_from_sorted_values(sorted_values):
    if len(sorted_values)==0:
        return None
    max=len(sorted_values)//2
    root=Node(sorted_values[max])
    root.left= _build_bst_from_sorted_values(sorted_values[: max])
    root.right= _build_bst_from_sorted_values(sorted_values[max+1 :])
    return(root)
x=[8,5,14,1,7,10,20]
root= _build_bst_from_sorted_values(sorted(x))
print("BST before insertion:")
for i in root.values:
    print(i,'-->',end="")
x.append(int(input()))    
root= _build_bst_from_sorted_values(sorted(x))
print("\nBST after insertion:")
for i in root.values:
    print(i,'-->',end="")
```

## OUTPUT
<img width="1198" height="342" alt="image" src="https://github.com/user-attachments/assets/ebd50710-2d13-412d-986b-6111bd8fd53d" />

## RESULT
->The program constructs a BST from the given list of elements.

->Inserting a new element and rebuilding ensures the tree remains balanced and maintains the BST property.

->Displaying root.values shows the updated inorder traversal before and after insertion.
