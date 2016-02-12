# If Statements

In the previous chapters, you learned all about logical operators and comparison operators. These form the basis for writing boolean expressions in if statements.

We use if statements to run a segment of code only if some boolean expression first evaluates to true. An if statement takes the following basic form:

```
if (boolean expression) 
{
    //Segment of code that will run if the boolean expression is true
}
```

If the boolean expression evaluates to false, nothing will happen. The code within the if statement is ignored. 

## If/Else Statements

We can add the **else** keyword to our if statement. In this case, if the boolean expression in our if statement evaluates to false, the code within the **else** segment will run. If the boolean expression evaluates to true, the code within the if segment will run.

```
if (boolean expression) 
{
    //Segment of code that will run if the boolean expression is true
} 
else 
{
    //Segment of code that will run if the boolean expression is false
}
```

## If/Else/Else If Statements

We can add the **else if** keyword between our if/else statement. If *boolean expression one* evaluates to false, then *boolean expression two* gets evaluated next. If *boolean expression two* also turns out to be false, the code within the `else` segment will run.

```
if (boolean expression one) 
{
    //Segment of code that will run if boolean expression one is true
} 
else if (boolean expression two)
{
    //Segment of code that will run if boolean expression two is true
}
else 
{
    //Segment of code that will run if boolean expression one and boolean expression two are both false
}
```

You can have as many **else if** statements as you want. There is no limit!

## Test for Negative Numbers

Using if statements, we can determine if a number is negative. If a number is less than 0, we know it is a negative number.

```
public class TestForNegatives extends ConsoleProgram
{
    public void run()
    {
        System.out.println("This program tests if a number is negative.");
        int number = readInt("Enter a number: ");
        if (number < 0) 
        {
            System.out.println("You entered a negative number!");
        }
    }
}

```


## Age Survey

Suppose we want to ask users for their age, but we want to restrict them from being able to enter a negative number. After all, someone can not have a negative age. We can accomplish this by doing the following:

```
public class AgeSurvey extends ConsoleProgram
{
    public void run()
    {
        int age = readInt("How old are you? ");
        if (age < 0) 
        {
            System.out.println("You can't have a negative age!");
        }
        else
        {
            System.out.println("Your age: " + age);   
        }
    }
}
```

If the user enters a negative age (less than 0), our program informs them that is not allowed. Otherwise, it prints their age back out to them.

## Improved Age Survey

We can improve our age survey even further by restricting users from being able to enter ages that are too large. We do this by adding in an **else if** statement.

```
public class ImprovedAgeSurvey extends ConsoleProgram
{
    public void run()
    {
        int age = readInt("How old are you? ");
        if (age < 0) 
        {
            System.out.println("You can't have a negative age!");
        }
        else if (age > 123)
        {
            System.out.println("No one has ever lived to the age of " + age + "!");
        }
        else
        {
            System.out.println("Your age: " + age);   
        }
    }
}
```

With these restrictions, we have created a range of acceptable ages. Valid ages are considered between 0 and 123 inclusive. If a user enters an age that is less than 0, we tell them that is impossible. If a user enters an age over 123, we inform them that no one has ever lived that long before. Otherwise, we simply print their age.


## Even or Odd

We want to write a program that tests whether some given number is even or odd. Here is how that can be done.

```
public class EvenOrOdd extends ConsoleProgram
{
    public void run()
    {
        int num = readInt("Number: ");
        if(num % 2 == 0)
        {
        	System.out.println("Number is even.");
        }
        else
        {
        	System.out.println("Number is odd.");
        }
    }
}
```

Recall that the modulous

## Logical Operators in Boolean Expressions

In the previous examples, we have been using comparison operators in our boolean expressions. We will now write a program which combines the usage of comparison operators with logical operators. This program will check to see if someone's numerical grade is a B.

```
var grade = readInt("What grade did you get? ");
if (grade >= 80 && grade < 90) {
    grade = "You got a B!";
} else {
    grade = "You did not get a B.";
}
println(grade);
```