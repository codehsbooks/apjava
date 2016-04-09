# Class Design and Abstract Classes
<hr>
One of the biggest challenges in Java is taking the time to actually write out relations between classes. It is incredibly important to understand how each class relates to one another. It is also important to know the characteristics that define each class.


### Class Design
<hr>
Lets take a look at the ***Vehicle Class*** from the previous chapter.
![Vehicle Class](../static/classesAndOOP/Class_and _oop_Inheritance_Tree.png)

In this diagram we can see that both ***Car Class*** and ***Motor Cycle Class*** inherit from ***Vehicle Class***. While ***Truck***, *** Sports Car***, and ***S.U.V.*** extend ***Car Class***. This diagram demonstrates the relations between our subclass and superclass.


### Abstract Classes
<hr>
Unlike an ordinary class, ***abstract classes*** can't be instantiated. This means that you can not create new instances of an ***abstract class***, as you would an ordinary class. While you can't instantiate an ***abstract class***, it can still share properties or be related to the subclass. 

#### Creating an Abstract Class

#### Creating Abstract Methods