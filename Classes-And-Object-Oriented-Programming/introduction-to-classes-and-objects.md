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

A behavior of the car may be to get the mileage from the remaining fuel.

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
    
    public String toString()
    {
        String rectInfo = "Rectangle with width: " + width + " and height: " + height + 
            " and area: " + getArea();
            
        return rectInfo;
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
    
    public String toString()
    {
        String aInfo = "This animal's name is: " + name + " they are currently a pet: " +
            isAnimalPet + ". The animal is " + age + " years old.";
            
        return aInfo;
    }
}
```
##### Vehicle Class
Here is another example of a class that takes in a vehicle type, its age, and how many miles it has:

``` Java
public class Vehicle
{
    private String vehicleType;
    private int vehicleAge;
    private double vehicleMiles;
    
    public Vehicle(String vType, int vAge, double vMiles)
    {
        vehicleType = vType;
        vehicleAge = vAge;
        vehicleMiles = vMiles;
    }
    
    public String getType()
    {
        return vehicleType;
    }
    
    public int getAge()
    {
        return vehicleAge;
    }
    
    public double getMiles()
    {
        return vehicleMiles;
    }
    
    public double estimateMilesPerYear()
    {
        return vehicleMiles / vehicleAge;
    }
}

```
## Creating Objects

When creating a new object from a class you will use the following format:

``` Java 
[Class Name] [Object Name] = new [Class Name] (params);

// Here are some examples using the classes we created earlier

Rectangle rect = new Rectangle(20, 8);

Animal pet = new Animal("Cujo", true, 7);

Vehicle myTruck = new Vehicle("Truck", 10, 173600.4);

```

## State and Behavior

As discussed earlier, objects have both a state and behavior. Here are some examples on how to create objects with our previous defined classes, and use them.

``` Java
// Rectangle Class
public class StateBehavior_Rectangle
{
    // Here we will create a new rectangle, and then print its information.
    public void run()
    {
        // Create the rectangle
        Rectangle rect = new Rectangle(20, 8);
        // This will print ""Rectangle with width: 20 and height: 8 and area: 160"
        System.out.println(rect);
    }
}

// Animal Class
public class StateBehavior_Animal
{
    // Here we will create a new animal, and then print its information.
    Animal myPet = new Animal("Cujo", true, 7);
}
// Vehicle Class

```