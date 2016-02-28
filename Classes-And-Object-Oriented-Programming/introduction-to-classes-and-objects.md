# Introduction to Classes and Objects

Classes and Objects are utilized in Java as part of the Object Oriented Programming model. This model focuses on objects and the data and actions associated with the objects.

## Object

Objects are structures that contain a state and behavior. 
Every day objects we commonly use have states and behaviors. For example, a car is an object. A car has both a state and a behavior.

##### State
The state contains the information about the specific object. 

Thinking back to the car in this case. An example of a state, with the car, would be how much fuel it has.

##### Behavior
The behavior is the actions that can be performed on the specific object.

A car may be able to get its mileage from the remaining fuel.

## Classes
Classes are the templates we use for creating objects.

##### Rectangle Class
Here is an example of a class that lets us create a rectangle, and get its area:

``` Java
public class Rectangle
{
    private double width;
    private double height;
    
    public Rectangle(double rectWidth, double rectHeight)
    {
        width = rectWidth;
        height = rectHeight;
    }
    
    public int getWidth()
    {
        return width;
    }
    
    public int getHeight()
    {
        return height;
    }
    
    public int getArea()
    {
        return width * height;
    }
}
```
##### Animal Class
Here is another example of a class that lets us create new animal objects:

```Java
public class Animal
{
    private String name;
    private boolean isPet;
    private int age;
    
    public Animal(String animalName, boolean isAnimalPet, int animalAge)
    {
        name = animalName;
        isPet = isAnimalPet;
        age = animalAge;
    }
    
    public String getName()
    {
        return name;
    }
    
    public boolean getPetStatus()
    {
        return isPet;
    }
    
    public int getAge()
    {
        return age;
    }
}
```
##### Vehicle Class
``` Java
public class Vehicle
{
    private String vehicleType;
    private int vehicleYear;
    private double vehicleMiles;
    
    public Vehicle(String vType, int vYear, double vMiles)
    {
        vehicleType = vType;
        vehicleYear = vYear;
        vehicleMiles = vMiles;
    }
    
    public String getType()
    {
        return vehicleType;
    }
    
    public int getYear()
    {
        return vehicleYear;
    }
    
    public double getMiles()
    {
        return vehicleMiles;
    }
}

```
## Creating Objects

When creating a new object from a class you will use this format:

``` Java 
[Class Name] [Object Name] = new [Class Name] (params);

// Here are some examples using the classes we created earlier

Rectangle rect = new Rectangle(20, 8);

Animal pet = new Animal("Dog", "Cujo", 2);

Vehicle myTruck = new Vehicle("Truck", 2000, 173600.4);
```