# Ex. No: 15D - Implementation of Min-Heap Using Python heapq Module

## AIM:
To demonstrate the creation of a min-heap from a list of elements using Python’s built-in heapq module.
## ALGORITHM:
```
1.Import the heapq module.
2.Define a function heaptree(H) that:
    ->Uses heapq.heapify(H) to convert the input list H into a min-heap.
    ->Prints the heapified list, which maintains the heap property (parent ≤ children).
3.Input a list of elements (integers or floats) from the user.
4.Call the heaptree() function with the input list.
```
## PROGRAM:

```
import heapq
def heaptree(H):
    heapq.heapify(H)
    print("The created Heap is",H)
```

## OUTPUT
<img width="1172" height="192" alt="image" src="https://github.com/user-attachments/assets/ddd8f0b3-a4a0-4364-89cf-2ecd47fd7ddc" />


## RESULT
->The program successfully converts a given list into a min-heap.

->The smallest element is at the root (index 0).

->The heap can be used for efficient extraction of the minimum element or other heap operations.
