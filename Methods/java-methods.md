# Java Methods

To teach Karel a new word, we had to create a method that contained instructions for Karel to follow. Though we are no longer programming with Karel, we can still use methods to organize our code in a similar way.


## Methods in Java

Methods allow us to break our program down into smaller parts by grouping commands together. Methods are useful because they help us avoid having to repeat the same sequence of commands over and over. As you recall, to have Karel turn right, you could give Karel three `turnLeft();` commands. But it was much easier to create a `turnRight` method to "teach" Karel how to turn right instead of writing out `turnLeft();` three times over and over.

Let's say we want to write a program that prints out your favorite skateboard tricks and draws ASCII art of a skateboarder between every word. Your program might look like this:

```
public class SkateVocab extends ConsoleProgram
{
    public void run()
    {
        System.out.println("Nollie big spin");
        System.out.println("      |    ");
        System.out.println("      /o   ");                                                                                  
        System.out.println("     /     ");
        System.out.println("   _/o     ");
        
        System.out.println("Tre flip");
        System.out.println("      |    ");
        System.out.println("      /o   ");                                                                                  
        System.out.println("     /     ");
        System.out.println("   _/o     ");
        
        System.out.println("A super clean kickflip");
        System.out.println("      |    ");
        System.out.println("      /o   ");                                                                                  
        System.out.println("     /     ");
        System.out.println("   _/o     ");
        
        System.out.println("180 no-comply");
        System.out.println("      |    ");
        System.out.println("      /o   ");                                                                                  
        System.out.println("     /     ");
        System.out.println("   _/o     ");
    }
}
```

Drawing out the skateboard so many times becomes quite tedious. Instead of writing out four lines of System.out.println(), it would be much easier to create a "draw skateboard" method.

```
public class SkateVocab extends ConsoleProgram
{
    public void run()
    {
        System.out.println("Nollie big spin");
        drawSkateboard();
        
        System.out.println("Tre flip");
        drawSkateboard();
        
        System.out.println("A super clean kickflip");
        drawSkateboard();
        
        System.out.println("180 no-comply");
        drawSkateboard();
    }
    
    private void drawSkateboard()
    {
        System.out.println("      |    ");
        System.out.println("      /o   ");                                                                                  
        System.out.println("     /     ");
        System.out.println("   _/o     ");
    }
}
```

Using a method makes the program easier to read and understand. Also, if you ever want to change the ASCII art picture of the skateboard, you would only need to do it once in the method instead of changing it througout the program.
