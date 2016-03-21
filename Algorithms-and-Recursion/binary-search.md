# Binary Search
Linear search is a fantastic implementation of a search algorithm, but it assumes the list is not sorted. Using a binary search algorithm we can skip half of the list, and return what we are looking for much faster.

##### How Binary Search Works
Using binary search, we will choose high and low indexes. The algorithm will then grab the item at the middle index and compare it to what we are searching for. If the element is less than our key we discard the half that is larger, and vice versa. Finally, we search through the remaining half of our list until we come across the key. 

