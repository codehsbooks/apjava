# ArrayList Methods
Arrays are amazing, but they lack flexibility and useful methods. That's where ArrayList comes into play. An ArrayList is similar to an Array, except that it is resizable and has more functionality. 

### ArrayLists
You can think of an ArrayList as a container that will resize as we add/remove objects from it. ArrayLists can't store primitive types so we must use ``Integer`` for ints and ``Double`` for doubles

<.Gif example here>

### Creating ArrayLists
We create an ArrayList in a similar fashion as if we were to create an Array. To create an ArrayList we use: `ArrayList<type> variableName = new ArrayList<type>();`

Lets say we want to create an ArrayList that holds the grades for a class. Here is an example of what that code would look like:

```Java
// Import the ArrayList
import java.util.*;

public class ArrayListExample extends ConsoleProgram
{
  public void run()
  {
    // Create the ArrayList named `classGrades` and set its type to `Integer`
    ArrayList<Integer> classGrades = new ArrayList<Integer>();
    
    // Add the grades to our ArrayList
    classGrades.add(97);
    classGrades.add(50);
    classGrades.add(80);
    classGrades.add(90);
  }
}
```

Now we want to create a list of students in a classroom. We can use the ArrayList for this as well:

```Java

```
### Using ArrayLists

### Iterating Over ArrayLists


