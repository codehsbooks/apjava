# Loop and a Half

Recall that while loops execute as long as their condition is true. Repeating code while a condition is true can be very useful; for example, the `frontIsClear()` condition can be used to have Karel repeatedly move until the front is no longer clear. But what happens if the condition is always true?

## The Infinite Loop

Infinite loops can occur unintentionally if you are not careful with the conditions of a while loop. In these cases, the infinite loop can cause the program to crash. However, infinite loops can be a very useful tool in programming. If your program needs to repeat a block of code an indefinite number of times, an infinite loop may be the correct approach.

Here's how to set up a basic infinite loop:

    while(true)
    {
        // code to execute
    }
    
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
    
