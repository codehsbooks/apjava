# Loop-and-a-Half

Recall that while loops execute as long as their condition is true. Repeating code while a condition is true can be very useful; for example, the `frontIsClear()` condition can be used to have Karel repeatedly move until the front is no longer clear. But what happens if the condition is always true?

## The Infinite Loop

Infinite loops can occur unintentionally if you are not careful with the conditions of a while loop. In these cases, the infinite loop can cause the program to crash. However, infinite loops can be a very useful tool in programming. If your program needs to repeat a block of code an indefinite number of times, an infinite loop may be the correct approach.

Here's how to set up a basic infinite loop:

    while(true)
    {
        // code to execute
    }
    
### Breaking out of a Loop
    
Repeating code is nice, but it's just as important to be able to stop the loop so that the rest of the program can continue executing. Loops can be stopped using the `break` statement. When the loop encounters a `break` statement, it quits running the loop and program flow continues.

    while(true)
    {
        // code to execute
        
        if(condition)
        {
            // if the condition is true, stop looping
            break;
        }
    }

### Stopping with Sentinels

Notice how in the previous example, the `break` statement occurs when a certain condition is true. Checking for a condition like this is a useful way to have the while loop repeat as many times as needed. This is especially true when getting input from the user. For example, you may want to print out numbers from the user until the program encounters the value `-1`. Such a program may look like this:

    while(true)
    {
        int num = readInt("Enter an integer: ");
        if(num == -1)
        {
            break;
        }
        System.out.println(num);
    }

We can clean up this code by using a variable instead of writing `-1` in the body of the program. This variable acts as a sentinel value that signals the end of the loop. As such, we'll name the variable `SENTINEL`:

    int SENTINEL = -1;
    
    while(true)
    {
        int num = readInt("Enter an integer: ");
        if(num == SENTINEL)
        {
            break;
        }
        System.out.println(num);
    }

Using a sentinel value allows us to change the condition quickly and easily; for example, you can change the sentinel from `-1` to `0` and the loop will stop when the user enters `0`.

## Why Use a Loop-and-a-Half?

It may seem dangerous or time-consuming to use an infinite loop, but when used appropriately, the loop-and-a-half structure is efficient and effective. The loop-and-a-half structure is preferred because it avoids repeating code outside and inside the loop. Furthermore, it is often easier to reason through the logic behind a loop-and-a-half. For example, with a simple program that prints numbers to the screen:

- Loop-and-a-Half:

public class PrintNumbersA extends ConsoleProgram
{
    public void run()
    {
        double SENTINEL = -1;

        while(true)
        {
            int num = readInt("Enter an integer: ");
            if(num == -1)
            {
                break;
            }
            System.out.println(num);
        }
        System.out.println("Done!");
    }
}

- Repeated code:

public class PrintNumbersB extends ConsoleProgram
{
    public void run()
    {
        int num = readInt("Enter an integer: ");

        while(num != -1)
        {
            System.out.println(num);
            num = readInt("Enter an integer: ");
        }
        System.out.println("Done!");
    }
}

The second example `PrintNumberB` reads in user input both outside and inside the loop. By using `while(true)`, the loop-and-a-half structure only reads in the variable inside the loop. This cuts down on repeated code and avoids confusion.

