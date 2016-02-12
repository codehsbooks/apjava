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

We can add the **else** keyword to our if statement.In this case, if the boolean expression in our if statement evaluates to false, the code within the **else** segment will run. If the boolean expression evaluates to true, the code within the if segment will run.

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

## Age Survey

Suppose we want to ask users for their age, but we want to restrict them from being able to enter a negative number. After all, someone can not have a negative age. We accomplish this by doing the following:

```
var age = readInt("How old are you? ");
if (age < 0) {
    age = "You can't have a negative age!";
}
println("Your age: " + age);
```

## Even or Odd

We want to write a program that tests whether some given number is even or odd. Here is how that can be done.

```
var num = readInt("Number: ");
if(num % 2 == 0){
	println("Number is even.");
}else{
	println("Number is odd.");
}
```

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