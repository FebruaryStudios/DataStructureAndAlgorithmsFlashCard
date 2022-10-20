# Tree

## Problem tree data structure was trying to solve

Given a Dictionary/Set, look up value using a key:
Two implementations:

- Using contigous data structure (Array)
- Using LinkedList data structure

**Contigous data structure**  
**Array implmentation** ( Unsorted & Sorted)

| Operation       | Sorted Array | Unsorted Array |
| --------------- | :----------: | -------------: |
| Search(key)     |  0 (log N)   |           0(N) |
| Insert(key,val) |     0(N)     |           0(1) |
| Delete(key)     |     0(N)     |           0(N) |

**Hashtable** : Hash function + Array
Using the Hash function, we map index in array to improve Search performance
Avoid collision - 2 keys maping to same index ( good Hash function can avoid this.)

| Operation       |                   Hashtable                   |
| --------------- | :-------------------------------------------: |
| Search(key)     |       0(1) Hash function calc key, A[k]       |
| Insert(key,val) | 0(1) Hash function calc key, set A[k] = value |
| Delete(key)     | 0(1) Hash function calc key, set A[k] = null  |

**LinkedList implementation** (Unsorted & Sorted)
