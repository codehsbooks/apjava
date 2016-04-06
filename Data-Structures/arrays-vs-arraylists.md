# Arrays vs ArrayLists
<hr>
Both Arrays and ArrayLists are incredibly useful to programmers, but how do we know when to use them? While both Arrays and ArrayLists perform similar operations, they are used differently.

### Differences Between Arrays and ArrayLists
<hr>
One the biggest differences between an Array and ArrayList is expandability. While the size of an ArrayList can change, an Array is a set size. Other differences include handling types and getting the size/length.

##### Getting the Size or Length:
How we retrieve the size or length of an Array or ArrayList varies between the two.
<br>
When dealing with an ***Array*** we use ``arr.length`` to access its length.
<br>
With ***ArrayLists*** we would use ``list.size()``.

##### Setting Values at an Index:
Settings values at a given index varies as well.
<br>
To set the value of a given index with an ***Array*** we use ``arr[i] = x;``.
<br>
To set the value of a given index with an ***ArrayList*** we use ``list.set(i, x);``.

##### Getting Values at an Index:
To retrieve values at a given index is as follows:
<br>
To get a value at a given index with an ***Array*** we use ``int x = arr[i];``.
<br>
To get a value at a given index with an ***ArrayList*** we use ``int x = list.get(i);``.

##### Creating New Instances:
To create new instances of an Array or ArrayList you use:
<br>
To create a new instance of an ***Array*** we use ``int[] arr = new int[5];``.
<br>
To create a new instance of an ***ArrayList*** we use ``ArrayList<Integer> list = new ArrayList<Integer>();``.

##### Extra Helper Methods:
Only ArrayLists have extra helper methods. These helper methods include: remove, add at index, clear, and isEmpty.
<br>

##### Types:
***Arrays*** can hold Primitives or Objects.
<br>
***ArrayLists*** can only hold Objects, and handles autoboxing and unboxing.
<br>