20220712:0950
Tags: #computing 
Backlinks:
# Quicksort
Quicksort is a sorting algorithm. As the name suggests, it is very efficient.

The basic technique is to choose a pivot (often the last element in the range to be sorted), and then move every element in range that is greater than the pivot to its right, and vice versa to the left. The pivot will be in the right position, and subsequently the sections to the left and right of it can be sorted in order to sort the entire range.

```python
def qs(arr, l, r):
	# when -l == r, there is only one element in the range
	if l >= r:
		return
	p = partition(arr, l, r)

	qs(arr, l, p - 1)
	qs(arr, p + 1, r)

def partition(arr, l, r):
	pivot = arr[r]
	i = l - 1
	for j in range(l, r):
		if arr[j] < pivot:
			i += 1
			temp = arr[i]
			arr[i] = arr[j]
			arr[j] = temp

	temp = arr[i + 1]
	arr[i+1] = arr[r]
	arr[r] = temp
	return i + 1
```
Worst case is O(n^2)
Best case is O(n)

Standard quicksort doesn't work especially well when there are a lot of duplicates in the array. There is an alternate method for handling these kinds of arrays called 3-way quicksort, which essentially involves splitting the array into three partitions; a group that is less the pivot, one that is equal to the pivot, and one that is greater than the pivot.

---
# References
[📽CS Dojo: A Complete Overview of Quicksort](https://www.youtube.com/watch?v=0SkOjNaO1XY)