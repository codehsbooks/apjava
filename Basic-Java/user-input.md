# User Input

Being able to obtain user input creates new opportunities while coding. Being able to see what the user wants allows us to take in data and make our programs work for the user.

## Getting User Input

In Java there are four ways we can obtain user input:

| Input | Description |
| -- | -- |
| ``readLine("String prompt")`` | Allows us to ask the user to input a **string**. |
| ``readInt("String prompt")`` | Allows us to ask the user to input an **integer**. |
| ``readDouble("String prompt")`` | Allows to ask the user to input a **double**. |
| ``readBoolean("String input")`` | Allows us to ask the user to input a **boolean**. |

## Input of Strings

To read the user's input as a string, we use ``readLine("String prompt")``. This allows us to ask the user for their name, favorite color, or any other text input from the user.

Here is an example of how we would ask the user for their favorite color, and then print it:

```java
// Ask for the input, and store it in the 'favColor' string.
String favColor = readLine("Hello, what is your favorite color? ");
// Then print it.
System.out.println(favColor);
```

## Input of Integers

To read the user's input in an integer format, we would use ``readInt("String prompt")``. This allows us to ask the user for their age, favorite number, or any other whole number. 

Here is an example of how we would ask the user for their age, and then print it:

```java
// Ask for the input, and store it in the 'age' integer.
int age = readInt("Hello, how old are you? ");
// Then print it.
System.out.println(age);
```

## Input of Doubles

To read the user's input as a double, we use ``readDouble("String prompt")``. This allows us to ask the user how many miles they have traveled, how much an item costs, or any other numerical value that has a decimal.

Here is an example of how we would ask the user for how many miles they have traveled, and then print the input:

```java
// Ask for the input, and store it in the 'miles' double.
double miles = readDouble("How many miles have you traveled? ");
// Then print it.
System.out.println(miles);
```

## Input of Booleans

To read the user's input as a boolean, we use ``readBoolean("String prompt")``. This allows us to ask the user any true or false question.

Here is an example of how we would ask the user if they are a astronaut, and then print their answer:

```java
// Ask for the input, and store it in the 'isAstronaut' boolean.
boolean isAstronaut = readBoolean("Hello, are you an astronaut? ");
// Then print it.
System.out.println(isAstronaut);

```



















