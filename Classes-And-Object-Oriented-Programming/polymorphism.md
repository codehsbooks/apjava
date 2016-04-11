# Polymorphism
<hr>
***Polymorphism*** is one of the most important concepts in Object Oriented Programming.
<br>
<br>
***Polymorphism*** is the capability of a single object to take on multiple forms. ***Polymorphism*** can also be explained as the ability to perform a single action in many ways across multiple objects. It also allows us to use the same method across different objects, using different implementations. 

### Polymorphism Concepts
<hr>
There are several concepts of ***polymorphism*** that are crucial to remember. These include:

- **Upcasting: ** Occurs when the reference variable of a super class refers to the object of the subclass. This allows us to go from a low level class type to a higher level one.

- **Downcasting: ** Occurs when the reference variable of a subclass refers to the object of the superclass. This allows us to go from a high level class type to a lower level one.

- **Dynamic Binding: ** The concept where the proper method implementation is chosen at run-time, and not compile-time.

- **Static Binding: ** The concept where the proper method implementation is chosen at compile-time, and not run-time.

- **Method Overriding: ** Allows us to call the correct implementation of a method across multiple objects that share the same superclass.

### Upcasting:
<hr>
Now that we know ***upcasting*** refers to taking an object of a lower level class type and referencing it to a class of a higher level, lets look at some examples:

```Java

```

### Dynamic Binding
<hr>
***Dynamic Binding*** is a very important concept to ***runtime polymorphism***. Now that we understand that it is the concept of the proper method implementation being chosen at run-time, lets look at some examples:

```Java

```

### Static Binding
<hr>
***Static Binding*** is another important concept to ***polymorphism***. Unlike ***dynamic binding**, **static binding** chooses the proper method implementation at compile-time, and not run-time. Lets look at some examples of this concept:

```Java


```

### Method Overriding
<hr>
***Method Overriding*** allows us to use the same method across multiple objects with differing implementations. Lets take a look at some examples of this concept:

```Java

```

### Polymorphic Arrays
<hr>
***Polymorphic Arrays*** allow us to store an array of objects with differeing types that share the same superclass. Lets see this in action:

```Java

```



