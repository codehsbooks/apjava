# 2D Arrays (Matrices or Grids)
Imagine a video game company contacts you to build Tic-Tac-Toe game. As part of the game development process, you'd need to figure out a method of storing each player's turn. How would we achieve this? Java has a two-dimensional array data structure that we can use. 2D Arrays, also known as Matrices or Grids, can are essentially an "array of arrays."

### Creating 2D Arrays
To create a 2D Array, we would use: ``type[][] name = new type[rows][columns];``

Here are some examples:

```Java
// Create a 2x4 grid of doubles
double[][] doubleGrid = new double[2][4];
 
// Create a 5x6 grid of Strings
String[][] stringGrid = new String[5][6];

// Create a 6x10 grid of chars
char[][] charGrid = new char[6][10];

// Create a 3x3 grid of integers
int[][] intGrid = new int[3][3];

// Initializing our Tic-Tac-Toe Grid with X's (1's) as the winner.
int[][] gameBoard = {
  {1, 0, 2},
  {0, 1, 2},
  {0, 0, 1}
 };
```
<br>

### What 2D Arrays Look Like
If you were to visualize a 2D Array, it would be easiest to think of it like a table of values:

Here is what a 3x3, 2D Array would look like:

|   | 0 | 1 | 2 |
| --- | --- | --- | --- |
| **0** |``(0, 0)``|``(1, 0)``|``(2, 0)``|
| **1** |``(0, 1)``|``(1, 1)``|``(2, 1)``|
| **2** |``(0, 2)``|``(1, 2)``|``(2, 2)``|
Where the top and far left rows represent our **X** and **Y** indexes. 

### Utilizing 2D Arrays
Now that we understand what 2D Arrays look like, and how to create them, we can focus on utilization. 

Let's say we have a 3x3 grid, named `gameBoard`, with the value of our Tic-Tac-Toe game. In this case, `0` represents a blank space, `1` represents a **X**, and `2` represents an **O**.

Here is what our grid looks like with **X** as the winner:

|   | 0 | 1 | 2 |
| --- | --- | --- | --- |
| **0** | 1 | 0 | 2 |
| **1** | 0 | 1 | 0 |
| **2** | 2 | 2 | 1 |

##### Getting an Element:
Let's say we want to access a specific element of our grid. For this, we use: `int elem = grid[row][col];`.
With that said, we want to grab the element in the middle of the grid. So we would use: `int elem = gameBoard[1][1];`, which would give us a `1`.
Now, we want to get the element in the top right corner of the canvas. In this case, we use: `int elem = gameBoard[2][0];` and we get `2`.

##### Setting an Element:
In order to set an element of a grid we use: `grid[row][col] = elem;`.
If we wanted to make **O** the winner of our game we would have to set the elements at `(0, 0)` and `(0, 1)` to `2`. In order to do this we would use:
```Java
gameBoard[0][0] = 2; 
gameBoard[0][1] = 2;
```

Now our Grid looks like:

|   | 0 | 1 | 2 |
| --- | --- | --- | --- |
| **0** | 2 | 0 | 2 |
| **1** | 2 | 1 | 0 |
| **2** | 2 | 2 | 1 |

##### Getting a Row:
Finally, to get a specific row of a grid, we use `int[] row = grid[row];`.
If were were to access the values in the 2nd row of our board, we would use `int[] 2ndRow = gameBoard[1];`.



