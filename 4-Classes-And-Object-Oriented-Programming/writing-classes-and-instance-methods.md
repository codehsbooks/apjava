# Writing Classes and Instance Methods
<hr>
***Instance methods*** allow us to define the behavior of an object.
<br>
Lets say you are wanting to get the area of a specific rectangle object you created using the `Rectangle` class. To do this, you would need to define an ***instance method*** that will return the area of our rectangle object. It is important to remember that ***instance methods*** belong to the specific instance of your object. 

### Creating Instance Methods
<hr>

The general form of an instance method is as follows:
```Java
[visability] [returnType] name(parameters)
  public       double    getArea()
  private       int      truncateArea()
```

The ***visibility*** of your method determines if it can be used outside your object's class. This is usually *public* or *private*.

The ***returnType*** is the type of our return value. If there is no return value for the method we use *void*.

The ***name*** is the name of our method.

The ***parameters*** is the list of our parameters, or the information we give to the method.

<br>

Here is what our `Rectangle` class looks like:

```Java
public class Rectangle
{
    // Instance variables
    private double width;
    private double height;
    
    public Rectangle(double rWidth, double rHeight)
    {
        width = rWidth;
        height = rHeight;
    }
    
    // Our instance method
    public double getArea()
    {
        return width * height;
    }
}
```

### Using Instance Methods
<hr>

To call instance methods we use the following format: `objectName.methodName(parameters);`
<br>
<br>
The ***objectName*** is the name of the object we are calling the method on.
<br>
The ***methodName*** is the name of the instance method we are calling.
<br>
The ***parameters*** are the inputs we give the method (if any).

In practice, this looks like:

```Java
Rectangle rect = new Rectangle(7, 10);

// Get the area of our rectangle by calling instance method `area();`
double rectArea = rect.getArea();
```
