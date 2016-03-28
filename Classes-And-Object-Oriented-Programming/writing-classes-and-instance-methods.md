# Writing Classes and Instance Methods
<hr>
***Instance methods*** allow us to define the behavior of an object.
<br>
Lets say you are wanting to get the area of a rectangle object you created using the `Rectangle` class. To do this, you would need to define an ***instance method*** that will return the area of our rectangle object. It is important to remember that ***instance methods*** belong to the specific instance of your object. 

### Creating an Instance Method
<hr>

The general form of an instance method is as follows:
```Java
[visability] [returnType] name(parameters)
  public       double    area(width, height)
  private       int      truncateArea(width, height)
```