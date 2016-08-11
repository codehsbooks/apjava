# Comparison Operators

Comparison operators allow us to compare two values against one another. A comparison returns a boolean result of either **true** or **false**. The table below lists each of the common comparison operators and their usages:

|  Operator      |  Usage           |  
| -------------- | ---------------- |
| >              | Greater Than     |  
| <              | Less Than        |  
| >=             | Greater Than Or Equal To|  
| <=             | Less Than Or Equal To|   
| ==             | Equal To   |          
| !=             | Not Equal To |   

## A Basic Comparison

In the following example, we compare two variables `x` and `y`. We store the result of this comparison in variable `z`.

```
int x = 10;
int y = 8;

boolean z = x > y;
System.out.println(z);
```
What will get printed to the screen? The above comparison, x > y, is evaluating if 10 is greater than 8. Because 10 is indeed greater than 8, `z` is assigned a value of true. Thus, `true` will get printed to the screen.

## More Practice with Comparisons

Let's get a little more practice. Take a look at the following code segment below. Pay close attention to each comparison and the operator being used.


```
// Declare some integer variables to use for practice comparisons below.
int a = 3;
int b = 5;
int c = 2;
int d = 3;

// We store the boolean results of each comparison into boolean variables t-z.
boolean t = a > 0;
boolean u = a == d;
boolean v = d >= b;
boolean w = b > c;
boolean x = a != d;
boolean y = d < = a;
boolean z = 4 < = c;

/* In addition to integers, it is possible to compare other data types too.
   Here we are comparing some of the boolean values computed above (t-z).
   We store the results into new boolean variables. */
boolean boolComparison1 = t == u;
boolean boolComparison2 = t == w;
boolean boolComparison3 = t != u;
boolean boolComparison4 = x != y;
```
```
// Print out all the integer comparison results
System.out.println("t = " + t);
System.out.println("u = " + u);
System.out.println("v = " + v);
System.out.println("w = " + w);
System.out.println("x = " + x);
System.out.println("y = " + y);
System.out.println("z = " + z);

// Print out all the boolean comparison results
System.out.println("boolComparison1 = " + boolComparison1);
System.out.println("boolComparison2 = " + boolComparison2);
System.out.println("boolComparison3 = " + boolComparison3);
System.out.println("boolComparison4 = " + boolComparison4);

```


When we run this code, what boolean values (**true** or **false**) will get printed to the screen for variables t through z? What boolean values (**true** or **false**) will get printed to the screen for each of the boolComparison variables? See if you can figure it out on your own. The solution is given below.

####Solution:

Our program prints out:

```
t = true
u = true
v = false
w = true
x = false
y = true
z = false
boolComparison1 = true
boolComparison2 = true
boolComparison3 = false
boolComparison4 = true
```

## Comparison Operators in a Program

Suppose we want to write a program which restricts people under a certain height from riding on a roller coaster. For this particular roller coaster, people who are under 4 feet (48 inches) are not allowed on the ride. How would we do this?

```
int heightInInches = readInt("How tall are you (in inches)? ");
boolean isTallEnough = heightInInches >= 48;
System.out.println("Can ride on the roller coaster: " + isTallEnough);
```

After getting the potential rider's height in inches, we do a comparison to ensure that they are over 48 inches. The result of this comparison is then printed out.

## Pitfalls

A common mistake is using `=` when you actually want to use `==`. `=` is used for assignment of variables whereas `==` is used for comparing the equality of two values.

For example, `x = 5` stores the value `5` into the variable `x`. However, `x == 5` tests to see if the value `5` is equal to the variable `x` and then returns either true or false. **They are not the same thing!**
