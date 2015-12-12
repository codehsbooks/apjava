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

To read a user's input in a string value we use ``readLine("String prompt")``. This allows us to ask the user for their name, favorite color, or any other text input from the user.

Here is an example of how we would ask the user for their favorite color, and then print it:

```java
String favColor = readLine("Hello, what is your favorite color? ");
System.out.println("Your favorite color is: " + favColor);
```

## Input of Integers

## Input of Doubles

## Input of Booleans