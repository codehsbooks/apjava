# Key Terms for Classes

You've likely noticed that learning a programming language involves learning a lot of new vocabulary terms. Let's review some of the key concepts and terms that we've learned so far.

## Objects and Classes

Not surprisingly, objects are a key part of object-oriented programming. Let's review some of the important concepts of objects and classes.

#### What is an Object?

An **object** is something that contains both state and behavior. It is an instance of a class.

A **class** is a template for creating an object.

An **instance** is what you call a specific version of a class. Instances and objects generally refer to the same thing.

For example, if you owned a factory that produced bikes, you would likely want blueprints or plans for each type of bike. Mountain bikes would a blueprint, BMX bikes would have a different blueprint, and road bikes would have their own blueprint. These blueprints are like **classes** in programming. The plans for each class can produce a specific **object**. If you were to follow the plans to build a road bike, the object you end up with could be called an **instance** of the "RoadBike" class.

#### State and Behavior

Objects have state and behavior. An object's state is store in variables, while its behavior is defined by methods. State and behavior can be specific to a single instance of a class (for example, one specific road bike), or shared between all the members of a class.

An **instance method** is a method called on an instance of a class, or an object, that helps define the behavior of the class.

An **instance variable** is a variable belonging to an instance of a class, or an object, that helps define the state of the class.

An **class method** or static method is a method called on the class. It does not have an object as the receiver. It is accessible to all instances of the class.

A **class variable** or static variable is a variable belonging to the class, not any object instance. It is accessible to all instances of the class.

## Packages

A benefit of using classes and objects is that they can potentially reduce the amount of code that you need to rewrite. To create a new road bike, you don't need to rewrite all of the road bike code. You can simply instantiate a new instance of the "RoadBike" class.

This same type of code reusability is present in other aspects of the Java programming language as well. You may find yourself wanting to use and reuse related classes that you or other programmers have already designed. Rather than rewriting classes each time, classes can be bundled into **packages** and imported into your code.

You import classes from a package like:
`import packageName.*;`

You import a single class like
`import packageName.ClassName;`

## Visibility

Some of the code you write should be accessible to everyone, but you may often want to limit who or what can access certain parts of your code. You can help ensure that an object's state and behavior can only be modified properly by setting the **visibility** of classes, methods, and variables.

**Public** visibility means that the object, method, or variable is open for use by everyone. Most of the classes we write in this course are public. Something is decalred public by using the `public` keyword: `public class RoadBike`

**Private** visibility limits access. Most of the instance variables we write are private, which prevents them from being changed by others. The `private` keyword is used to declare something as private: `private int costOfBike;`

The levels of access each type of visibility provides can be summarized in a table:

visibility | Class | Package | World (everyone) |
--- | --- | --- | --- |
**public** | yes | yes | yes |
**private** | yes| no | no |

## What is This?

It can often be confusing to know whether a variable in a constructor is referring to an instance variable or a variable that was passed in as an argument to the constructor. One way around this is to use different variable names for the instance variables and parameters.

```
public class BMX
{
	private String frameSize;
	private int numPegs;

	public BMX(String theFrameSize, int theNumPegs)
	{
		frameSize = theFrameSize;
		numPegs = theNumPegs;
	}
}
```

Notice that the constructor's parameters are `theFrameSize` and `theNumPegs` instead of `frameSize` and `numPegs`.

Using different names can get a little confusing. Fortunately, Java has a way of specificying when you are referring to the object itself: **this**.

`this` refers to the current object. The `this` keyword allows us to be very clear whether we are referring to the object's instance variable or a parameter:

```
public class BMX
{
	private String frameSize;
	private int numPegs;

	public BMX(String frameSize, int numPegs)
	{
		this.frameSize = frameSize;
		this.numPegs = numPegs;
	}
}
```
