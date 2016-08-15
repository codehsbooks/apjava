# Class Methods and Class Variables

## Classes and Instances

Recall that an object is an instance of a class. The class is like the blueprint from which instances can be built. Each instance can have its own state and behavior. An object's state is stored in instance variables, and its behavior is carried out with instance methods. These are called **instance variables** and **instance methods** because they belong to a single instance of the class.

But what if you wanted to keep track of a single variable or have a shared behavior across *all* the members of a class? Because each object has its own instance variabes and methods, these won't work to store information for the entire class.

## Class Methods and Class Variables
Sometimes it is useful to store information that is shared across all the objects of an entire class. A **class variable** is a variable or attribute of a class that is common to all instances of a class. A **class method** is a method of a class that is common to all instances of a class and is not called on any specific object instance. These are sometimes referred to as **static variables** and **static methods**.

A new static variable or method is defined by adding the keyword `static` to the variable or method declaration. A method to return the total number of birds of the Bird class may look like:
```
private static int getTotalBirds()
{
    return totalBirds;
}

```

## Skating and Coding
For example, if you ran your own indoor skatepark, you may want to keep track of the skaters at the park. In order to use the park, a new skater would sign up and an new instance of the `Skater` class would be created. What information would be useful to track about each skater? You may want to know a skater's name, age, experience level, and a history of times he or she arrived at and left the park. These are all unique to each skater and could be stored as instance variables.

It would also be useful to know how many skaters have ever skated at the park. This is a useful stat to know, but it is affected by all the skaters, not just one. Because this information is shared across the whole class, it can be stored in a class variable. The `Skater` class could be defined to include these:

```
public class Skater
{
    private static int totalSkaters = 0;
    
    public Skater()
    {
        totalSkaters++;
    }
    
    public static int getTotalSkaters()
    {
        return totalSkaters;
    }
}
```
Whenever a new skater is added, the static variable `totalSkaters` is increased. The `totalSkaters` variable is shared across all instances of the `Skater` class. Each object in the class has the same value for this variable, and we can get the value of this variable with the static `getTotalSkaters` method.

## Using Static Methods and Variables
Because static methods and variables are available across an entire class, they don't need to be called on a particular instance of the class. You do not need to create a new object just to call a class method.

To find out how many skaters have been to the skatepark, you can write:
```
Skater.getTotalSkaters();
```

This will call the `getTotalSkaters()` method on the `Skater` class without requiring an instance of the class to be created.


