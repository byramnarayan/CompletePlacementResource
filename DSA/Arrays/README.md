# Arrays

## Introduction

An array is a data structure that contains a collection of elements, typically of the same data type, stored in ** contiguous ** memory locations. Arrays are used to store multiple values in a single variable, which can be accessed using an index.

## Types of Arrays

1. **Static Arrays**: Fixed size arrays where the size is determined at the time of declaration and cannot be changed.
2. **Dynamic Arrays**: Arrays that can grow or shrink in size during runtime.

## Operations on Arrays

1. **Traversal**: Accessing each element of the array.
   - **Time Complexity**: O(n)
2. **Insertion**: Adding an element at a specific position.
   - **Time Complexity**: O(n) (worst case, when inserting at the beginning)
3. **Deletion**: Removing an element from a specific position.
   - **Time Complexity**: O(n) (worst case, when deleting from the beginning)
4. **Searching**: Finding the location of an element in the array.
   - **Time Complexity**: O(n) (linear search), O(log n) (binary search on sorted array)
5. **Sorting**: Arranging the elements in a particular order (ascending or descending).
   - **Time Complexity**: O(n log n) (average case for efficient algorithms like quicksort, mergesort)


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
