# How to Indent Your Code
Indentations are an important part of the structure of your code. Indentations make your code easier to read and understand, and are a key part of good style.

## Indenting Your Code

A general rule for Java is to ***always*** place brackets on their own lines, and indent the code within the brackets. Here is an example for you to reference:

```
// Notice how the brackets are on new lines and the code within is indented.
public void run()
{  
    move();
    turnLeft();
    move();
}
```

You apply the same rule for indentations when using nested control structures. Consider this example:

```
// Notice how the brackets are on new lines and the code within is indented.
public void run() 
{
    while(ballsPresent())
    {
        if(frontIsClear())
        {
            move();
        }
    }
}
```


## Practice Questions

**1)** Consider the following piece of code:
```
public class WalkRoadKarel extends SuperKarel
{
public void run()
{
    while(frontIsClear())
    {
        move();
    }
}
}
```
<p> Does this piece of code have proper indentations? </p>
- [ ] ``` while(facingNorth()) { turnLeft(); }```
- [x] ``` while(notFacingNorth()) { turnLeft(); } ```
 
> Very close! Double check the condition in the loop. Remember, we want to turn when Karel is not facing North.

> This is the correct answer! Nice job!


