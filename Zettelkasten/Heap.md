20220712:0843
Tags: #computing 
Backlinks:
# Heap
A heap is a tree-like data structure. It comes in two forms; a max heap where each node is greater than its children, or a min heap, where each node is lesser than its children.

In a heap, inserted elements are always added in the next available position, from top->bottom and left-> right. If the element is not in the correct place, it can be "bubbled up" and swapped with its parent until it's positioned correctly.

Because the next element in a heap is always going to be inserted in the same place, they can be represented as an array. The following can then be used to find nodes relative to a node at a given index:
- To find the parent node: (index - 2) / 2
- To find the left node: index * 2 + 1
- To find the right node: index * 2 + 2

A common method used on heaps is to poll them, where the root element is removed and replaced by the last element in the array, and then the heap is adjusted (ie swapped around) until correct.

Popping from a heap is takes O(logn) time.

---
# References
[📽Gayle Laakmann: Heaps](https://www.youtube.com/watch?v=t0Cq6tVNRBA)