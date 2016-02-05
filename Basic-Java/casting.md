# Casting

Casting allows us to change a variable's type to better suit our needs. 

## How Casting Works

Lets say we want to turn a double into an integer, or an integer into a double.

To change a variable's type we just add the type in between parentheses to cast it. 

Consider the following:

``` Java
int doubleToInt = (int)10.95;
double intToDouble = (double)5;
```

##### Casting an Integer to a Double

To cast an integer value to a double we add ``(double)`` in front of the variable.

``` Java
int intVal = 10;

// Our 'doubleVal' variable is now '10.0'
double doubleVal = (double)intVal; 
```
##### Casting a Double to an Integer

To cast a double to an integer we add ``(int)`` in front of the variable.
It is important to remember our new integer value will truncate the decimal.

``` Java
double doubleVal = 7.4;

// Our 'intVal' variable is now '7'
int intVal = (int)doubleVal;
```

## Division with Casting

If we divide two integers, even if we are setting them to a double, we will always be returned an integer.

``` Java
int currResidents = 50;
int floorTotal = 56;

double average = floorTotal / currResidents;
```