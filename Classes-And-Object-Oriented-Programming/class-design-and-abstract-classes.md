# Class Design and Abstract Classes
<hr>
One of the biggest challenges in Java is taking the time to actually write out relations between classes. It is incredibly important to understand how each class relates to one another. It is also important to know the characteristics that define each class.


### Class Design
<hr>
Lets take a look at the ***Vehicle Class*** from the previous chapter:
![Vehicle Class](../static/classesAndOOP/Class_and _oop_Inheritance_Tree.png)

In this diagram we can see that both ***Car Class*** and ***Motor Cycle Class*** inherit from ***Vehicle Class***. While ***Truck***, *** Sports Car***, and ***S.U.V.*** extend ***Car Class***. This diagram demonstrates the relations between our subclass and superclass.


### Abstract Classes
<hr>
Unlike an ordinary class, ***abstract classes*** can't be instantiated. This means that you can not create new instances of an ***abstract class***, as you would an ordinary class. While you can't instantiate an ***abstract class***, it can still share properties or be related to the subclass. 

#### Creating an Abstract Class
In order to create an ***abstract class*** you must add the keyword: `abstract` to the class declaration.

Here are a couple of examples of abstract classes in Java:

```Java
// Here is our Vehicle Class
public abstract class VehicleClass {

}

// Here is an example of our Shape class
public abstract class Shape {

}
```
#### Creating Abstract Methods
***Abstract methods*** are methods that are declared within an abstract class, but lack implementation. In most cases you would have to implement the method within the subclass. This way you have more flexibility with subclasses that require different logic in the same method.

Here is an example of ***abstract methods*** using our ***Vehicle Class***

```Java
public abstract class VehicleClass
{
  private String type;
  private String vehicleName;
  
  public VehicleClass(String vType, String vName)
  {
    type = vType;
    vehicleName = vName;
  }
  
  /* This will need to be abstract, since 
   * we will need to implement different formulas
   * depending on if the vehicle is electric or 
   * gas powered.
   */ 
  public abstract double getMileage();
}

/* As you can see, in both classes, we have `getMileage` implemented
 * with different formulas.
 */ 
public class Truck extends VehicleClass
{
  private double gasTankCapacity;
  private double milesPerTank;
  
  public Truck(double capacity, double miles)
  {
    gasTankCapacity = capacity;
    milesPerTank = miles;
  }
  
  public double getMileage()
  {
    return milesPerTank/gasTankCapacity;
  }
}

public class ElectricCar extends VehicleClass
{
  private double maxCharge;
  private double milesPerCharge;
  private double maxEnergyUsage;
  
  public ElectricCar(double charge, double maxEnergy)
  {
  
  }
  
  public double getMileage()
  {
  
  }
}

```

