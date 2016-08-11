# Arithmetic Expressions
Arithmetic Expressions allow us to perform mathematical operations within Java. 

Such expressions can be used for basic math and even more complex algorithms.

## Arithmetic Operators

| Operator | Description|
| --- | --- |
| + | Addition operator (Ex. 1 + 1 = 2) |
| - | Subtraction operator (Ex. 2 - 1 = 1) |
| * | Multiplication operator (Ex. 2 * 2 = 4) |
| / | Division operator (Ex. 6 / 2 = 3) |
| % | Modulus operator (Ex. 10 % 3 = 1) |


##### Addition Operator

The addition operator allows us to add values together. 

Here is an example of the addition operator in Java:

```Java

public class AdditionOperator extends ConsoleProgram
{
    public void run()
    {
        int firstVal = 5;
        int secondVal = 2;
        
        int firstPlusSecond = firstVal + secondVal;
        
        // The output will be '7'
        System.out.println(firstPlusSecond);
    }
}

```

##### Subtraction Operator

The subtraction operator allows us to subtract values from one another.

Here is an example of the subtraction operator in Java:

```Java
public class SubtractionOperator extends ConsoleProgram
{
    public void run()
    {
        int firstVal = 4;
        int secondVal = 2;
        
        int firstMinusSecond = firstVal - secondVal;
        
        // The output will be '2'
        System.out.println(firstMinusSecond);
    }
}
```

##### Multiplication Operator

The multiplication operator allows us to multiply values. 

Here is an example of the multiplication operator in Java:

```Java
public class MultiplicationOperator extends ConsoleProgram
{
    public void run()
    {
        int firstVal = 4;
        int secondVal = 2;
        
        int firstMultSecond = firstVal * secondVal;
        
        // The output will be '8'
        System.out.println(firstMultSecond);
    }
}
```

##### Division Operator

The division operator allows us to divide values.

Here is an example of the division operator in Java:

```Java
public class DivisionOperator extends ConsoleProgram
{
    int firstVal = 6;
    int secondVal = 3;
    
    int firstDivSecond = firstVal / secondVal;
    
    // The output will be '2'
    System.out.println(firstDivSecond);
}
```

##### Modulus Operator

The modulus operator allows us to divide two numbers, and get the remainder.

Here is an example of the modulus operator in Java:

```Java
public class ModulusOperator extends ConsoleProgram
{
    int firstVal = 17;
    int secondVal = 5;
    
    int firstModSecond = firstVal % secondVal;
    
    // The output will be '2' since the remainder of 17 / 5 is 3.
    System.out.println(firstModSecond);
}
```

## Operation Precedence

It is important to remember that the order of operations still apply. In instances where you have multiple operators with the same precedence the order will be, left to right.

| Operator | Precedence|
| --- | --- |
| ``( )`` Parenthesis | 1st |
| ``* /`` Multiplication and Division | 2nd |
| ``+ -`` Addition and Subtraction | 3rd |

## Types of Divison

There are multiple types of division that can be performed in Java. These forms include: integer division, double division, and mixed division.

##### Integer Division

If you divide two integers you will be returned an integer value.

So in this case, while ``2 / 5 = 2.5``, in Java ``2 / 5 = 2``. This always holds true, unless the type is specified as a double. Whenever you divide two integers, the return value is always truncated.

##### Double Division

Dividing doubles is different from dividing integers. 

When you divide two doubles you will be returned a double. In this case, ``2.0 / 5.0 = 2.5`` will be your result. 

##### Mixed Division

Mixed division is when you divide a double by an integer, or an integer by a double.

When you used mixed division in your program you will be returned a double. This is true, unless the type is specifically defined as an integer.

Consider the following piece of code:

```Java
double x = 2;
int y = 5;

double outXY = x / y;      // 0.4

double outYX = y / x;      // 2.5

int outInt = (int)(y / x);    // 2
```

## Arithmetic Shortcuts

There are shortcuts available when performing arithmetic expressions.

Consider the following table:


| Original | Shortcut | Description |
|---|---|---|
| ``counter = counter + 1;`` | ``counter++;`` | Increment a variable by ``1`` |
| ``counter = counter - 1;`` | ``counter--;`` | Subtract ``1`` from a variable |
| ``x = x + y`` | ``x += y`` | Adding values to a variable |
| ``x = x - y`` | ``x -= y`` | Subtracting values from a variable |
| ``x = x * y;`` | ``x *= y`` | Multiplying values to a variable |
| ``x = x / y;`` | ``x /= y`` | Dividing values from a variable |
