# Interfaces
<hr>
Interfaces in Java allow us to create a collection of methods to guarantee a class's interaction. An interface does not contain method implementation, constructors, or instance variables.

Interfaces are commonly used to help achieve polymorphism.

### Implementing Interfaces
<hr>

To implement an interface we use the `implements` keyword after our class name, like: `public class Dog implements Animal`. In this case `Dog` is our class name, where `Animal` is our interface.

Let's look at an interface for using a computer. We will call it `UseComputer`.

```Java
public interface UseComputer
{
  /* Notice how we end our method signatures with semi-colons `;`
   * and not curly brackets
   */ 
  public void pressKey(Key keyPressed);
  public void clickMouse(MouseEvent mouse);
  public void shutDown();
  public void startUp();
}
```

Now, let's take a look at an example class which implements our interface:

```Java
public class GeneralUser implements UseComputer 
{
  private boolean isShuttingDown = false;
  private boolean isStartingUp = false;
  
  public void pressKey(Key keyPressed)
  {
    return keyPressed;
  }
  
  public void clickMouse(MouseEvent mouse)
  {
    return mouse;
  }
  
  public void shutDown()
  {
    isShuttingDown = true;
    isStartingUp = false;
  }
  
  public void startUp()
  {
    isShuttingDown = false;
    isStartingUp = true;
  }
}
```

As you can see, we store the method signatures in our `UseComputer` interface, and implement them within our `GeneralUser` class.


### Comparable Interface
<hr>

Java is full of interfaces that you are free to utilize within your code. One interface you should become familiar with is the Comparable interface. The Comparable interface can be incredibly useful with sorting algorithms.

Here is what an implementation of the Comparable interface looks like:

```Java
// Marbles class, implements Comparable
public class Marbles implements Comparable<Marbles>
{
  private String owner;
  private int quantity;
  
  public Marbles(String ownerName, int mQuantity)
  {
    owner = ownerName;
    quantity = mQuantity;
  }
  
  public String getOwner()
  {
    return owner;
  }
  
  public int getQuantity()
  {
    return quantity;
  }
  
  public void setOwner(String newOwner)
  {
    owner = newOwner;
  }
  
  public void setQuantity(int newQuantity)
  {
    quantity = newQuantity;
  }
  
  public int compareTo(Marbles comMarbles)
  {
    int comQuantity = comMarbles.getQuantity();
    
    return getQuantity() - comQuantity;
  }
}

// Our main class
public class MarblesProgram extends ConsoleProgram 
{
    public void run()
    {
        Marbles marbles1 = new Marbles("Wezley", 10);
        Marbles marbles2 = new Marbles("James", 20);
        Marbles marbles3 = new Marbles("Kurt", 10);
        
        System.out.println(marbles1.compareTo(marbles2));
        System.out.println(marbles1.compareTo(marbles3));
    }
}
```


