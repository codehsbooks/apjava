# Interfaces
<hr>
Interfaces in Java allow us to create a collection of methods to guarantee a class's interaction. An interface does not contain method implementation, constructors, or instance variables.

Interfaces are commonly used to help achieve polymorphism.

### Implementing Interfaces
<hr>

To implement an interface we use the `implements` keyword after our class name, like: `public class Dog implements Animal`. In this case `Dog` is our class name, where `Animal` is our interface.

Lets look at the interface for `Animal`:

Our `Animal` interface will contain method signatures for various things an animal will do.

```Java
public interface Animal
{
  public double maxRunningSpeed();
  
}
```


### Interface Examples
<hr>
