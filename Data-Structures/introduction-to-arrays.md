# Introduction to Arrays
An array is a list of data. Arrays can store many different types of information. For example, if you had a shopping list, you could store the shopping list as an array.

## Organizing Information in an Array

The information stored in an array is kept in order. The items in an array are often referred to as *members* or *elements* of the array.

Unless we make changes to the array, the first element in the array will always be the first element, and the last item will always be last. It is important to note that in computer science, we usually start counting from 0. So the first item in the array is actually at index position 0, the second item in the array is at index position 1, and so on.

Let's say our grocery list contained these items, in this order: apples, dog food, donuts, celery, and orange juice. If we were to draw out the array, it would look something like this:

*index position:* | 0 | 1 | 2 | 3 | 4 |
---            |---|---|---|---|---|
***list item:***      |apples|dog food|donuts|celery|orange juice|

We can see that dog food is at index 1 and celery is at index 3.

## Creating Arrays
To create an array in Java, you must first know what type of data you want to store and how many elements the array will hold. In the grocery list example above, we created an array of Strings, but it's just as easy to create arrays of ints or any other data type. 

The format for creating an array is:

    type[] arrayName = new type[numberOfElements];

Let's take apart the array declaration:
- `type[]`: This tells us what type of data is being stored in the array. For example, a list of integers would be `int[]`. The brackets `[]` indicate that this is an array and not a single `int`.
- `arrayName`: The name by which the array will be known. It's best to pick a descriptive name, like `groceryList` instead of just `things`.
- `new`: The `new` keyword indicates that a new array is being created.
- `type[numberOfElements]`: The type of elements is mentioned again, as well as the number of items the array will store.

## Getting and Setting Array Elements
Once an array is declared, it's ready to store information. Perhaps the easiest way of putting data into an array is to initizalize the array with data when declaring it. To do so, simply include the array elements between curly braces. Here's a list of 6 numbers:

    int[] numberList = {10,20,30,40,50,60};
    
*index position:* | 0 | 1 | 2 | 3 | 4 | 5 |
---               |---|---|---|---|---|---|
***list item:***  |10 |20 |30 |40 |50 |60 |
    
#### Setting Elements
It's also possible to declare a new empty array and add in the list items later. Elements in an array can be accessed using the index position of the array. Let's create a new empty array of numbers, then add in two numbers:

    // Create an empty array that will store 6 integers
    int[] newNumberList = new int[6];
    
    // Add the number 11 to index position 0
    newNumberList[0] = 11;
    
    // Add the number 13 to index position 1
    newNumberList[1] = 13;
    
The array now contains two integers:

*index position:* | 0 | 1 | 2 | 3 | 4 | 5 |
---               |---|---|---|---|---|---|
***list item:***  |11 |13 |   |   |   |   |

The same syntax can be used to change elements in a list. Let's change 13 to 21:

    newNumberList[1] = 21;
    
*index position:* | 0 | 1 | 2 | 3 | 4 | 5 |
---               |---|---|---|---|---|---|
***list item:***  |11 |21 |   |   |   |   |

#### Getting Elements

Accessing elements in a list uses a similar syntax. We can get and store the number at index 0 into a variable:

    // This variable will contain the number 11
    int firstNumber = newNumberList[0];
    
    // Two ways to print out the number 11 to the console
    System.out.println(firstNumber);
    System.out.println(newNumberList[0]);
    
    // Now print out the number at index position 1 to the console
    System.out.println(newNumberList[1]);
    
The output from the code will be:

    11
    11
    21
