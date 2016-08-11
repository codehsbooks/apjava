# Writing Classes
Now that we have learned about what classes are... but wouldn't it be great if we could *write* our own classes? Well, it turns out  that we can! In this section, we will go over the different parts that make up a typical class in Java, parts that you will have to write yourself in order to make your class.

As a reminder, a class is a general blueprint for a certain type of object.  For example, we could have a class named `Dog` that serves as a general blueprint for objects of the type `Dog`.

```java
//Pretend that we have a class named Dog.  This defines what an object with the type Dog would be like.
public class Dog
{
    ...
}
...
...

//These are objects that have the type Dog!
Dog karel = new Dog();
Dog scoobyDoo = new Dog();
```

## What Goes Inside a Class?
Usually, most classes will include the following features:

1. Instance variables
2. Constructors
3. Methods

### Instance Variables
Hopefully, by now, you know what a variable is.  As a reminder, a variable is something that stores information.  An **instance variable** (sometimes also named **field** is a kind of variable that stores a certain piece information about an object created from a class.  It essentially represents a kind of information that is shared among other objects of the same class.  The kinds of instance variables a class contains will depend on what pieces of information you would want the class's objects to store! A class will declare what kinds of instance variables it would like its objects to have, and each object will have its own copy (also known as **instance**) of each instance variable declared in the class.

So let's use our `Dog` class example from before... What kind of instance variables would we want to put into a `Dog` class? Well, let's first think about what kinds of information that different `Dog` objects would share.  All dogs (we are not considering wild ones here) seem to have names.  That's one instance variable! What else other kinds of things are similar in dogs? Age seems to be another property that all dogs have.  That's another instance variable! These instance variables (as well as other instance variables) can be declared in the `Dog` class like this:

```java
public class Dog
{
    private String name;
    private int age;
    private double weight;
    private boolean isAlive;
    
    //This part will be continued below
    ...
}
```

### Constructors
Constructors are essentially **object creators**.  We use constructors to create new objects using a class.  When we create new objects using constructors, we also set any initial values of instance variables if necessary.  These initial values of instance variables can be set either with or without the use of parameters.

Here is the continuation of the above example showing how you would write a constructor:

```java
public class Dog
{
    private String name;
    private int age;
    private double weight;
    private boolean isAlive;
    
    public Dog(String theName, int theAge, double theWeight, boolean isThisAlive)
    {
        name = theName;
        age = theAge;
        weight = theWeight;
        isAlive = isThisAlive;
    }
}
```

In the above example, the variables in the parenthesis are the parameters that are passed in when you create a new `Dog` object.  This is how you would create a Dog object using the `Dog` class from above:

```java
Dog exampleDog = new Dog("Johnny", 17, 110.5, true);
```

That will create a new Dog named Johnny that has an age of 17, a weight of 110.5, and is alive.

It is good to know that you you are not forced to always have a parameter corresponding to an instance variable.  You are also allowed to set an instance variable for all objects to the same value, like this:

```java
public class Dog
{
    private String name;
    private int age;
    private double weight;
    private boolean isAlive;
    
    public Dog(String theName, int theAge)
    {
        name = theName;
        age = theAge;
        weight = 122.5;
        isAlive = true;
    }
}
```

In the above example, there are only two parameters (the parameters `theName` and `theAge`), but we decided to set the weight of ALL dogs to 122.5 and make ALL dogs alive.  So if you wanted to create a new dog using this constructor, you would only need to write this:

```java
Dog exampleDog = new Dog("Johnny", 17);
```

This example will create will create a new Dog named Johnny that has an age of 17, a weight of 122.5, and is alive.

### Methods
In the Karel Java exercises, we said that methods were like ways of teaching Karel new words/commands.  Here in non-Karel Java, methods are still essentially the same: they teach *the program* new commands.

We will go into more detail about methods in later sections.  For now, you should know about a specific kind of method that you can write into your classes: the `toString` method.  The `toString` just "converts" a class's object into something that you will be able to print out using `System.out.println`.

So for example, you could add a `toString` method to the `Dog` class from above, like this:

```java
public class Dog
{
    private String name;
    private int age;
    private double weight;
    private boolean isAlive;
    
    public Dog(String theName, int theAge, double theWeight, boolean isThisAlive)
    {
        name = theName;
        age = theAge;
        weight = theWeight;
        isAlive = isThisAlive;
    }
    
    public String toString()
    {
        return "This dog is named " + name;
    }
}
```

Notice how the `toString` method returns a `String`.  So to print out a `Dog` object, you would go like this:

```java
Dog exampleDog = new Dog("Johnny", 17);
System.out.println(exampleDog.toString());
```

That above snippet would print out:

```java
This dog is named Johnny.
```

## What Comes Next?

In this section, we went over the basic elements that make up a class in Java.  In the next sections, we will explore the details of writing classes.
