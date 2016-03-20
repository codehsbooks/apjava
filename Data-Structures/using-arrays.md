# Using Arrays
Arrays are utilized for many operations in various programs. Since arrays store data in order, we can iterate through them to access this data. Let's say we are creating an online store that sells oranges. We would want to store the customer orders in an array so we can honor the first orders before the orders that come later. 

### Accessing the Array

There are many ways we can access the items within our array.

Let's say we have an array that stores the order data from our market.
Here is the array:

| *Index:* | 0 | 1 | 2 | 3 | 4 | 5|
| --- | --- | --- | --- | --- | --- | --- |
| *Orders:* | 10 Oranges | 3 Oranges | 6 Oranges | 4 Oranges | 5 Oranges | 1 Orange |

In Java our array will look like:

```Java 
int[] orangeOrders = {10, 3, 6, 4, 5, 1};
```
<br>
##### Accessing a Single Element:
Our third order `index 2` is for 6 oranges, but what if the customer made a mistake and only wants 3 oranges? 

In this case we would access the array, and change the value at `index 2` to 6. To do this we would use:

```Java
orangeOrders[2] = 3;
```

The value at `index 2` in our array is set to 3.

<br>

Now, let's say orders at `index 4` and `index 5` paid for an express purchase. We need to push these two items into our order queue before the rest of our orders. To do this we would use `orangeOrders[4]` and `orangeOrders[5]`, and push them through our queue using `finalizeOrder(order);`.

Our code will look like:

```Java
finalizeOrder(orangeOrders[4]);
finalizeOrder(orangeOrders[5]);
```

##### Iterating Over The Array

It is the end of the day and our store has stopped accepting new orders. Now we need to send the current array of orders to be finalized. We don't want to access each item in the array one-by-one and rewrite code. So we will need to iterate over our array using a for loop. Since we are using a for loop, how do we know how many iterations it should perform? We use `arr.length` to see how many items are in our array.

Our code will look something like:

```Java
int[] orangeOrders = {10, 3, 6, 4, 5, 1};

for(int i = 0; i < orangeOrders.length; i++)
{
    finalizeOrder(orangeOrders[i]);
}
```

We can also iterate over our array to determine how many oranges have been sold using:

```Java
int[] orangeOrders = {10, 3, 6, 4, 5, 1};
int sumOfOranges = 0;

for(var i = 0; i < orangeOrders.length; i++)
{
  sumOfOranges += orangeOrders[i];
}

System.out.println("Total oranges sold: " + sumOfOranges);
```
