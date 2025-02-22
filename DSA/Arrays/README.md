# Arrays

## Introduction

An array is a data structure that contains a collection of elements, typically of the same data type, stored in ** contiguous ** memory locations. Arrays are used to store multiple values in a single variable, which can be accessed using an index.

## Types of Arrays

1. **Static Arrays**: Fixed size arrays where the size is determined at the time of declaration and cannot be changed.
2. **Dynamic Arrays**: Arrays that can grow or shrink in size during runtime.

## Operations on Arrays

1. **Traversal**: Accessing each element of the array.
   - **Time Complexity**: O(1)
   ## Diagram
   ![Reading](https://github.com/byramnarayan/CompletePlacementResource/blob/main/src/dsaImg/readingStaticArray.png)

2. **Insertion**: Adding an element at a end position.
   - **Time Complexity**: O(1) 
4. **Deletion**: Removing an element from a end position.
   - **Time Complexity**: O(1) 
   ## Diagram
   ![atEnd](https://github.com/byramnarayan/CompletePlacementResource/blob/main/src/dsaImg/insertRemoveAtEnd.png)

3. **Insertion**: Adding an element at a specific position.
   - **Time Complexity**: O(n) (worst case, when inserting at the beginning)
4. **Deletion**: Removing an element from a specific position.
   - **Time Complexity**: O(n) (worst case, when deleting from the beginning)
   ## Diagram
   ![atMiddle](https://github.com/byramnarayan/CompletePlacementResource/blob/main/src/dsaImg/insertRemoveMiddleStart.png)



## Advantages of Arrays

- **Random Access**: Elements can be accessed directly using their index.
- **Memory Efficiency**: Arrays have a fixed size, which can lead to efficient memory usage.

## Disadvantages of Arrays

- **Fixed Size**: Static arrays have a fixed size, which can lead to wasted memory or insufficient space.
- **Insertion/Deletion Overhead**: Inserting or deleting elements can be time-consuming as it may require shifting elements.

## Example Code

### Static Array in Python

```python
# Static Array
arr = [1, 2, 3, 4, 5]

# Traversal
for i in range(len(arr)):
    print(arr[i])

# Insertion
arr.insert(2, 10)  # Insert 10 at index 2

# Deletion
arr.pop(3)  # Remove element at index 3

# Searching
index = arr.index(4)  # Find index of element 4

# Sorting
arr.sort()  # Sort the array in ascending order



# Industry standard Code In Function

# Insert n into arr at the next open position.
# Length is the number of 'real' values in arr, and capacity
# is the size (aka memory allocated for the fixed size array).
def insertEnd(arr, n, length, capacity):
    if length < capacity:
        arr[length] = n

# Remove from the last position in the array if the array
# is not empty (i.e. length is non-zero).
def removeEnd(arr, length):
    if length > 0:
        # Overwrite last element with some default value.
        # We would also the length to decreased by 1.
        arr[length - 1] = 0

# Insert n into index i after shifting elements to the right.
# Assuming i is a valid index and arr is not full.
def insertMiddle(arr, i, n, length):
    # Shift starting from the end to i.
    for index in range(length - 1, i - 1, -1):
        arr[index + 1] = arr[index]
    
    # Insert at i
    arr[i] = n

# Remove value at index i before shifting elements to the left.
# Assuming i is a valid index.
def removeMiddle(arr, i, length):
    # Shift starting from i + 1 to end.
    for index in range(i + 1, length):
        arr[index - 1] = arr[index]
    # No need to 'remove' arr[i], since we already shifted

def printArr(arr, capacity):
    for i in range(capacity):
        print(arr[i])

```



### Dynamic Array in Python

```python
# Dynamic Array using list
dynamic_arr = []

# Insertion
dynamic_arr.append(1)
dynamic_arr.append(2)
dynamic_arr.append(3)

# Deletion
dynamic_arr.remove(2)  # Remove element 2

# Traversal
for element in dynamic_arr:
    print(element)
```
