# Tree

## Problem tree data structure was trying to solve

Given a Dictionary/Set, look up value using a key:
Two implementations:

- Using contigous data structure (Array)
- Using LinkedList data structure

## Contigous data structure

**Array implmentation** ( Unsorted & Sorted)

| Operation       | Sorted Array | Unsorted Array |
| --------------- | :----------: | -------------: |
| Search(key)     |  0 (log N)   |           0(N) |
| Insert(key,val) |     0(N)     |           0(1) |
| Delete(key)     |     0(N)     |           0(N) |

**Hashtable** : Hash function + Array:
Using the Hash function, we map index in array to improve Search performance
Avoid collision - 2 keys maping to same index ( good Hash function can avoid this.)

| Operation       |                   Hashtable                   |
| --------------- | :-------------------------------------------: |
| Search(key)     |       0(1) Hash function calc key, A[k]       |
| Insert(key,val) | 0(1) Hash function calc key, set A[k] = value |
| Delete(key)     | 0(1) Hash function calc key, set A[k] = null  |

## LinkedList implementation (Unsorted & Sorted)

Using the LikedList to solve our intial problem

| Operation       | Sorted List | Unsorted List |
| --------------- | :---------: | ------------: |
| Search(key)     |    0(N)     |          0(N) |
| Insert(key,val) |    0(N)     |          0(1) |
| Delete(key)     |    0(N)     |          0(N) |

How can we improve this T/C ( Search is the dominant operation)
We can tranform list to a tree (Search Tree) => e.g BST
**Property of BST**:

- All nodes to left sub tree is smaller than root
- All nodes to right sub tree is larger than root

| Operation       |          Hashtable           |
| --------------- | :--------------------------: |
| Search(key)     | 0(log N) Using binary search |
| Insert(key,val) |           0(log N)           |
| Delete(key)     |           0(log N)           |

## Summary : Implementing Dictionary/Set ADT

| Operation       | Hashtable | Balanced BST |
| --------------- | :-------: | -----------: |
| Search(key)     |   0(1)    |     0(log N) |
| Insert(key,val) |   0(1)    |     0(log N) |
| Delete(key)     |   0(1)    |     0(log N) |
