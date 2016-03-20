# Selection Sort
Lets say we are working on a statistics package that returns the median value of an array. The problem we run into is that the numbers in the array aren't sorted. First we must sort the numbers in the array from smallest to largest. Using Selection Sort is one way to sort the numbers in this array.


##### How it works

Selection Sort sorts the numbers in our array using loops to iterate over the arrays as we sort one number at a time. Each time the loop iterates we look for the smallest value left in the unsorted chunk and sort it. 

<--- Add .gif --->

##### How it looks

Here is an example of what a selection sort algorithm looks like:

```Java
public class SelectionSort extends ConsoleProgram 
{
  public void run() 
  {
    int[] intsToOrder = {10, 3, 6, 4, 5, 1};
     
    int minIndex = 0;
    int tmpValue = 0;
    for(int i = 0; i < intsToOrder.length; i++)
    {
      minIndex = i;
      for(int j = i + 1; j < intsToOrder.length; j++)
      {
        if(intsToOrder[j] < intsToOrder[minIndex])
        {
          minIndex = i;
        }
      }
      
      tmpValue = intsToOrder[minIndex];
      intsToOrder[minIndex] = intsToOrder[i];
      intsToOrder[i] = tmpValue;
    }   
  }
}

```
