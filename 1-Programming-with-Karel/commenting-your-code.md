# Commenting Your Code

There are two parts to writing a program: One part is getting it to work (the functionality). The other part is the style: How did you write the program? Did you break it down into parts? Is it clear to read? 

This is where comments come into play!

## Introducing comments

Comments are a way for you to leave notes about what your code is doing in plain English so that other people can understand it. 

### Why comment?

Even though code is run by computers, it is read by other people. Comments help others understand your code. If you read your code ten years from now, would you be able to understand what it does? 

The computer that runs your program knows not to ignore comments if they are written as multi-line or single line comments. 

### Multi-line comments

Use multi-line comments to leave a comment so a reader understands what your program or method is doing. The start of a multi-line comment uses ```/*```, each line following with a single ```*```, and ending the multi-line comment with ```*/```. 

    /* 
     * This program does ______. 
     */
     
### Single line comments

Use single line comments to leave a comment for a single line in your code. For each single line comment, put two backslashes (```//```) before the comment. 

    //This line does ______.
    
## Preconditions and postconditions

Another important part of commenting is using preconditions and postconditions. We can leave notes at the top of our methods about assumptions that we make.

**Preconditions**: What assumptions we make and what must be true **before** the method is called.

**Postconditions**: What should be true after the method has been called. 

This helps us think about the problem and make sure our methods line up.

## Example: Hurdle Karel with comments

Let's add comments to our Hurdle Karel program. First, we want to add a multi-line comment to describe what the program does at the top. 

    /*
     * This program has Karel run a race 
     * by jumping two hurdles. 
     */
    public class HurdleKarel extends Karel
    {
        ...
    }

Next, let's add another multi-line comment to describe what our method, ```run()```, does. 

    /*
     * This program has Karel run a race 
     * by jumping two hurdles. 
     */
    public class HurdleKarel extends Karel
    {
        /* 
         * This method is our main entry point for the program.
         * Karel runs to the hurdle and jumps it twice, before
         * finishing the race.
         * Precondition: Karel should be in the bottom left
         * corner, facing east.
         * Postcondition: Karel should be at the end of the race.
         */ 
        public void run()
        {
            runToHurdle();
            jumpToHurdle();
            runToHurdle();
            jumpToHurdle();
            finish();
        }
    }

Let's also add a multi-line comment for another method, ```runToFinish()```. 

        /* This method has Karel move four times to finish the race.
         * Precondition: Karel has finished jumping the last hurdle.
         * Postcondition: Karel is at the end of the race.
         */
	    private void runToFinish()
    	{
    	    move();
    		move();
    		move();
    		move();
    	}

In the runToFinish() method, we can add a single line comment. 

      private void runToFinish()
      {
            // This method has Karel move four times to finish the race.
            move();
    		move();
    		move();
    		move();
      }


### Full Example:

```/* 
 * This program has Karel run a race by jumping
 * two hurdles.
 */
public class HurdleKarel extends Karel
{

    /* 
     * This method is our main entry point for the program.
     * Karel runs to the hurdle and jumps it twice, before
     * finishing the race.
     * Precondition: Karel should be in the bottom left
     * corner, facing east.
     * Postcondition: Karel should be at the end of the race.
     */
	public void run()
	{
		runToHurdle();
		jumpHurdle();
		runToHurdle();
		jumpHurdle();
		runToFinish();
	}

    /* This method has Karel move four times to finish the race.
     * Precondition: Karel has finished jumping the last hurdle.
     * Postcondition: Karel is at the end of the race.
     */
	private void runToFinish()
	{
        // This method has Karel move four times to finish the race.
		move();
		move();
		move();
		move();
	}

    /* 
     * This method has Karel run to a hurdle that is three spots
     * away.
     * Precondition: Karel is three spaces away from a hurdle,
     * facing east.
     * Postconding: Karel is right next to a hurdle, ready to jump
     * over it.
     */
	private void runToHurdle()
	{
		move();
		move();
		move();
	}

    /*
     * This method has Karel jump over a hurdle that
     * is one row tall.
     * Precondtion: Karel is right next to a hurdle, facing east.
     * Postcondition: Karel has jumped over the hurdle and is on
     * the other side, facing east.
     */
	private void jumpHurdle()
	{
		turnLeft();
		move();
		turnRight();
		move();
		turnRight();
		move();
		turnLeft();
	}

    /* 
     * This method has Karel turn right.
     * Precondition: None, Karel can be facing any direction.
     * Postcondition: Karel will have turned right by 90 degrees.
     */
	private void turnRight()
	{
		turnLeft();
		turnLeft();
		turnLeft();
	}
}```