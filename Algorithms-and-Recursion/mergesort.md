# Mergesort
<hr>
Mergesort is one of the most efficient sorting algorithms you will learn about. Mergesort utilizes recursion to achieve efficient sorting of lists.

### How it works
<hr>

Mergesort utilizes what is known as a "Divide and Conquer" strategy. This means mergesort divides the problem into smaller parts until the array length is equal to one. Then it merges together adjacent arrays and sorts them until the whole list is sorted.

Lets see this in action:
![Mergesort Example](../static/algorithms/Algorithms_and_Recursion_Mergesort_Example.gif)
Here is another example:

![Mergesort Example](../static/algorithms/Algorithms_Mergesort_Example2.gif)

### Mergesort in Java
<hr>
Here is what mergesort looks like in Java:


```Java
import java.util.Arrays;

public class MergeSortExample extends ConsoleProgram 
{
  void run()
  {
  
  }
  
  void mergeSort(int[] list)
  {
    if(list.length > 1)
    {
      int firstHalf = list.length/2;
      int secondHalf = list.length - firstHalf;
      int[] listOne = new int[firstHalf];
      int[] listTwo = new int[secondHalf];
      
      System.arraycopy(list, 0, listOne, 0, firstHalf);
      System.arraycopy(list, firstHalf, listTwo, 0, secondHalf);
      
      mergeSort(listOne);
      mergeSort(listTwo);
      
      merge(listOne, listTwo, list);
    }
    return list;
  }
  
  void merge(int[] listOne, int[] listTwo, int[]finalList)
  {
  
  }
}

```

### Extra Notes
<hr>

It is important to know that if you utilize mergesort you will need to have extra space for temporary storage.

Mergesort is also recursive, meaning it calls upon itself.





