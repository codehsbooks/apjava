# Interfaces
<hr>
Interfaces in Java allow us to create a collection of methods to guarantee a class's interaction. An interface does not contain method implementation, constructors, or instance variables.

Interfaces are commonly used to help achieve polymorphism.

### Implementing Interfaces
<hr>

To implement an interface we use the `implements` keyword after our class name, like: `public class Dog implements Animal`. In this case `Dog` is our class name, where `Animal` is our interface.

Lets look at an interface for using a computer. We will call it `UseComputer`.

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

Now, lets take a look at an example class which implements our interface:

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

<br>
<br>

Here is another example of an interface. This interface will be used to

### Interface Examples
<hr>
