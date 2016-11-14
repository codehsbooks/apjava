# Objects vs Primitives

Not surprisingly, objects play a key role in object-oriented programming. But objects are not the only way that you will interact with data in the Java programming languages. Up to this point, you have built programs that include both objects and primitive data types. Understanding the differences between objects and primitives will help you plan and write programs.

### What is a Primitive?

Primitive data types are the basic building blocks of the Java programming language. These basic types cannot be broken down into other parts. Java includes several primitive types that you have seen before:

Type | Example
---  | ---
int  | int x = 42;
char | char oneChar = 'a';
double | double myNumber = 13.37;
boolean | boolean likesCoding = true;

These primitive types can be combined and used to build more complex objects. Primitive types are named with all lowercase letters.

### Primitives and Objects

Primitive data types are used to make objects. For example, a Movie object may have a title, director, whether it is a sequel, number of tickets sold, and runtime of the movie in minutes:

```
public class Movie
{
    private String title;
    private String director;
    private boolean isSequel;
    private int numTicketsSold;
    private double runtime;
}
```

#### Strings are not Primitives
Note that Strings are **not** a primitive data type. Strings are sequences of characters. As such, when creating a new string of text, be sure to capitalize the S in String: ```private String nyName```

### Making Comparisons
Comparing primitive data types like integers is straightforward using `==`. For example, to check if a user-entered number is 0:

```
int userNumber = readInt("Enter a number: ");
System.out.println(userNumber == 0);
```

The values of objects, however, cannot be compared with the `==`. Instead, objects are compared with a `.equals` method. For example:

```
String textOne = new String("Hello world!");
String textTwo = new String("Hello world!");
System.out.println(textOne.equals(textTwo));
```




