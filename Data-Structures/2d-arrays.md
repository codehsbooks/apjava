# 2D Arrays (Matrices or Grids)
<hr>
Lets say we are contracted by a video game company to build Tic-Tac-Toe game. We need to figure out a method of storing each player's turn to a grid. How would we achieve this? Luckily, Java allows us to utilize 2-Dimensional Arrays or Grids. A 2D Array can best be described as an "array of arrays."
<br>

### Creating 2D Arrays
<hr>
To create a 2D Array, we would declare it in a similar fashion as a regular Array. A 2D Array's declaration would look like: ``type[][] name = new type[rows][columns];``

Here are some examples:

```Java
// Create a 2x4 grid of doubles
double[][] doubleGrid = new double[2][4];

// Create a 5x6 grid of Strings
String[][] stringGrid = new String[5][6];

// Create a 6x10 grid of chars
char[][] charGrid = new char[6][10];

// Create a 3x3 grid of integers
int[][] intGrid = new int[3][3]

// Initializing our Tic-Tac-Toe Grid with X's (1's) as the winner.
int[][] gameBoard = {
  {1, 0, 2},
  {0, 1, 2},
  {0, 0, 1}
 };
```
<br>

### What 2D Arrays Look Like
<hr>

