# Using Arrays
Arrays are utilized for many operations in various programs. Since arrays store data in order, we can iterate through them to access this data. Lets say we are creating an online store that sells oranges. We would want to store the customer orders in an array so we can honor the first orders before the orders that come later.

### Accessing the Array

There are many ways we can access the items within our array.

Lets say we have an array that stores the order data from our market.
Here is the array:

| *Index:* | 0 | 1 | 2 | 3 | 4 | 5|
| -- | -- | -- | -- | -- | -- | -- |
| *Orders:* | 10 Oranges | 3 Oranges | 6 Oranges | 4 Oranges | 5 Oranges | 1 Orange |

In Java our array will look like:

```Java 
int[] orangeOrders = {10, 3, 6, 4, 5, 1};
```

