# Methods in Karel

In the last chapter, we briefly introduced using a method to turn Karel right. But what is a method? And why would we want to use them?


## The Basics

A method is a way to teach Karel a new word, or a new command. Methods allow us to break our program down into smaller parts and make it easier to understand. A program with many smaller methods is easier to read and fix than a program with one very large method.

The format of a method looks like:

    private void myMethod()
    {
        /* code goes here */
    }
    
## Naming is crucial

Here is another example: 

    private void buildPyramid()
    {
        /* code goes here */
    }

From the name of our method, ```buildPyramid()```, it is very clear what the method does. Be sure to name your methods descriptively. 

## Defining a method vs. calling a method

When we want to create and use new methods, there are two parts: Defining a method and calling our method after we have defined it. 

**Defining a method:** Teaching Karel the new word. In other words, writing out the instructions for this new action.

**Calling a method for Karel:** Actually getting Karel to do the command. Actually causing the action to happen.


### Example

**Defining ```turnRight()```**: Karel, when you want to turn right, the instructions are to turn left three times.

**Calling ```turnRight()```**: Karel, turn right.


