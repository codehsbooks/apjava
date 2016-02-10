# SuperKarel
Karel the Dog only knows a few basic commands. For example, in order to have Karel turn right, you first must create a new method to teach Karel how to turn right. Wouldn't it be nice if Karel already knew some of these commands?

## Introducing SuperKarel
Now that you've had some practice writing methods like `turnRight();`, you are ready to meet SuperKarel. SuperKarel already knows ```turnRight()``` and ```turnAround()```, so you don't need to create your own methods for those two commands anymore!

## Using SuperKarel
To write a Karel class, you extended `Karel`. To use SuperKarel, you will extend `SuperKarel` instead.

    // Regular Karel
    public class HurdleKarel extends Karel
    
    // SuperKarel
    public class HurdleKarel extends SuperKarel
    
## A SuperKarel Example
Using SuperKarel allows us to write fewer methods, since Karel already knows how to turn right and turn around. Below is an example of the HurdleKarel program using SuperKarel. Notice how the `jumpHurdle` method calls `turnRight();` even though this method is not defined in the program?

```
/* 
 * This program has Karel run a race by jumping
 * two hurdles. This is a SuperKarel program which
 * means turnRight() is built in.
 */
public class HurdleKarel extends SuperKarel
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

}
```
