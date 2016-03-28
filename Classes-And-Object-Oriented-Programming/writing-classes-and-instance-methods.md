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

The ***visibility*** of your method determines if it can be used outside your object's class. This is usually *public* or *private*.

The ***returnType*** is the type of our return value. If there is no return value for the method we use *void*.

The ***name*** is the name of our method.

The ***parameters*** is the list of our paramets, or the information we give to the method.

