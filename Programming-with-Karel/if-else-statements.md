# If/Else Statements
One of the driving forces behind writing conditionals is the need to vary the program's behavior based on certain conditions. When writing comprehensive conditionals, you will often want to have your program do something specifically when a particular if statement is evaluated as false. This is when the *else statement* becomes useful.


## Introducing If/Else Statements
Think of the else statement as the "otherwise" conditional. Consider the following pseudocode for an alarm clock function:
* 
If it is the weekend, go off at 10 AM.
* 
Otherwise, go off at 7 AM.

The "otherwise" clause allows us to account for all possible scenarios. In this example, we could have executed the same logic using two if statements, as follows:

* 
If it is the weekend, go off at 10 AM.
* 
If it is a weekday, go off at 7 AM.

However, when writing comprehensive programs, it may not be practical to account for every possible scenario. Suppose we want the alarm to go off at 7 AM on Tuesday and Thursday, and 8 AM on all other days. Using an "otherwise" clause, the logic is as follows:
* 
If it is Tuesday or Thursday, go off at 7 AM.
* 
Otherwise, go off at 8 AM.

Without using an "otherwise" clause, the logic follows:
* 
If it is Tuesday or Thursday, go off at 7 AM.
* 
If it is Sunday, Monday, Wednesday, Friday, or Saturday, go off at 8 AM.

It is clear that the former is more concise and pragmatic.

### If/Else Example
Suppose we want Karel to move if he can, and turn left otherwise. Keep in mind the following rules of thumb when writing if/else statements:
* 
Every else statement must be preceded by an if statement
* 
Not every if statement must have an else statement
* 
Else statements have no conditions, i.e., there are no parentheses following the "else"

Your code should then look like this:

```
if (frontIsClear())
{
    move();
} else
{
    turnLeft();
}
```

Note that, stylistically, the else statement may begin on the same line as the if statement's closing bracket, or on the following line. It is recommended that you stay consistent with whichever method you prefer. The code above may also be written as:

```
if (frontIsClear())
{
    move();
}
else
{
    turnLeft();
}
```


## If Statements vs. If/Else Statements

In general, else statements are not required.* You can usually achieve the effect of an else statement using a series of if statements. While this is valid, it is preferred that you use else statements for clarity and conciseness. 

*You may later be faced with scenarios in which else statements are required when writing helper functions with return values. More on this to come. 
