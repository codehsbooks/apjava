# While Loops

While loops are a way to repeat a block of code so long as some **condition** remains true. The condition is written in the form of a **boolean expression**. The basic structure of a while loop is shown below.

``` 
while(boolean expression)
{
    // code block inside of while loop to execute if the boolean expression is true
}
// code outside of while loop to execute if the boolean expression is false
```

As long as the boolean expression remains true, code within the while loop will be executed. The moment that the boolean expression becomes false, code outside of the while loop will be executed; the loop is done. This behavior can be summarized in the following flowchart below:

![While_Loop_Diagram](../static/karel/while_loop_diagram.png "While Loop Diagram") 


## While Loop Countdown

In the previous chapter, we looked at a simple program which counts down from 5 using a for loop. We can do the same thing using a while loop instead.

```
public class WhileLoopCountDown extends ConsoleProgram
{
    public void run()
    {
        int i = 5;
        
        System.out.println("Initiating countdown:");
        while(i >= 0)
        {
            System.out.println(i + "...");
            i--;
        }
    }
}
```

We first declare a variable `i` and set it equal to *5*. Before the while loop, we print out a message letting the user know that the countdown is about to begin. Our while loop starts by checking to see if the boolean expression, `i >= 0`, is true. The current value of `i` is *5*. `5 >= 0` is true, so the code within the while loop gets executed. It prints out the number *5* and then decrements it by subtracting 1. 

`i` is now set to *4*. Our while loop then checks to see if `4 >= 0`. Since this condition is still true, the code within the while loop gets executed again. This will continue until `i` gets down to *0*. After *0* gets printed to the screen, we decrement `i` so that it is now set to *-1*. Our while loop tests to see if `-1 >= 0`. Since *-1* is **not** greater than or equal to *0*, the boolean expression is false. The code within the while loop is skipped. The while loop has finished its execution.


After we run the above program, this is what gets printed to the screen:

```
Initiating countdown:
5...
4...
3...
2...
1...
0...
```

## Infinite Loops

You must exercise caution when using while loops to avoid the dreaded infinite loop. An infinite loop is a loop that never terminates. It never finishes its execution. It will continue to repeat until the end of time! Infinite loops will often cause a program to freeze and crash.

We have rewritten our while loop countdown program below, but we have omitted an essential line of code. This will cause an infinite loop:

```
public class InfiniteWhileLoopCountdown extends ConsoleProgram
{
    public void run()
    {
        int i = 5;
        
        System.out.println("Initiating countdown:");
        while(i >= 0)
        {
            System.out.println(i + "...");
        }
    }
}
```

But why? Why does this cause an infinite loop?

With the omission of `i--`, we are no longer changing our variable. `i` will forever be set to 5. Our while loop will repeatedly check to see if `5 >= 0`. Since this condition is *always* true, the code within the while loop body will execute forever. The while loop will *never* terminate. Our program will just keep printing a value of *5* over and over again.

Thus, after running the program, our output will look something like this (assuming the browser does not freeze and crash):

```
Initiating countdown:
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...
5...

[NOTE: This will continue printing "5..." forever!]
```

In the CodeHS editor, we can manually stop the program by clicking on the "STOP" button next to the "RUN CODE" button. Otherwise, it will continue spamming the number 5 at us until the end of time.


## While Loop or For Loop?

How do you decide whether to use a while loop or a for loop? After all, they are both used to repeat code segments.

For loops are for repeating code a **fixed** number of times. We use for loops when we know exactly how many times we want to repeat a given segment of code. We use while loops when we don't know how many times we will need to repeat some given code.

Consider the following program. In this program, the user attempts to guess a secret number between 1 and 100, but they don't know what that number is. We give them an unlimited number of guesses. If their guess is wrong, we have them guess again. If their guess is right, we inform them that they found the secret number and the program ends.

```
public class GuessTheSecretNumber extends ConsoleProgram
{
    public void run()
    {
        // The secret number for the user to guess is 54. But they don't know that!
        System.out.println("I am thinking of a secret number from 1 to 100. Can you guess it? ");
        int secretNumber = 54;
        
        // Read an integer guess from the user
        int guess = readInt("Type a number: ");
        while (guess != secretNumber)
        {
            guess = readInt("Incorrect. Try a different number: ");
        }
        System.out.println("Correct! You got it!");
    }
}
```

We don't know how many guesses it will take the user to find the secret number. It might take them only one or two guesses. It might take them over twenty or even over fifty guesses. We don't know! Thus, we must use a while loop here. A for loop won't do us any good. 

