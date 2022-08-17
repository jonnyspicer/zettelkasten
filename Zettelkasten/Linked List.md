20220702:2014
Tags: #computing 
Backlinks: [[Data Structures]]
# Linked List
A linked list is a data structure where each element contains a pointer to the next element in the list. The data can be sorted or unsorted, unique or duplicated, and any kind of data can be in the list.

One of the main differences between a linked list and an array is that an array is indexed, mean you can instantly access eg the 4th element, however this is not possible with a linked list. This means it takes O(n) time to get to the kth element (which is pretty slow!)

The main advantage is that insertion or deletion from the *beginning* of a linked list can be done in O(1) time, although appending to the *end* of a list will take O(n) time as the whole list will have to be traversed.

Lists can also be doubly linked - this is when each element contains both a pointer to the next element *and* a pointer to the previous element.

---
# References