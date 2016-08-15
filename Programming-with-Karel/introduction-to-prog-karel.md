# Introduction to Programming with Karel the Dog

Computers play an integral role in the modern world. From playing games to banking online, we interact with computers directly and indrectly every day. Understanding how computers work and how to work with them is an important skill. Computer programming is the process of giving commands to a computer. Sequences of commands can be combined into programs that perform specific tasks.

## Programming with Karel

Giving instructions to a computer is much like giving commands to a dog. In this course, we will learn the basics of programming with Karel the Dog.

Karel's world is a simple one: Karel can move around the world and put down and pick up tennis balls. Though Karel only knows a few commands, these commands can be combined into interesting programs to solve many different problems and explore the basics of computer science.


## Karel's Grid World

Karel's world is actually a grid. Each point on the grid is marked by a dot. Karel can move from point to point and travel around the world. The horizontal rows are called streets in Karel's world, and the vertical columns are referred to as avenues. In each spot, Karel can face four directions: north, south, east, or west.

## Karel's commands

In order to have Karel perform an action, you need to give Karel a command. A command is an instruction that tells Karel what to do.

Karel only knows four commands:

    move();
    putBall();
    takeBall();
    turnLeft();

### What does each command do?

The `move()` command has Karel move one spot in the direction that Karel is facing.

The `putBall()` command puts down one tennis ball in the spot where Karel is standing.

The `takeBall()` command removes one tennis ball from the spot where Karel is standing.

The `turnLeft()` command turns Karel 90 degrees to the left.

### The parts of a command

Notice that Karel's commands look a little different from plain English words. This is because Karel's commands are written as computer code. These simple spelling rules are called the *syntax* of Karel's language. There are a few things to keep in mind when writing commands for Karel:

* You need to write the command exactly as it appears in the list above.  

* You need to match the exact capitalization. For example, `turnleft();` is incorrect. It should be written as `turnLeft();` with an uppercase `L`.

* Make sure to end every command with a `();`

* Each command goes on its own line.

## Our First Karel Program

![Start and Ending World](https://www.evernote.com/shard/s4/sh/ecab1bdc-c74d-4394-b92c-11790f95a86f/c3b1398ee6eb5154c4a9601e3c03ec50/deep/0/Introduction-to-Programming-With-Karel---CodeHS.png)

Imagine you have Karel starting in the world on the left: in the bottom left corner, facing east. You want to get Karel to the world on the right. What would be the code that you write?

Remember, Karel has four commands, and we can use those commands to write this program. Below you can find the program.

Here's a program we could write to have Karel complete the task:

```
move();
move();
putBall();
move();
move();
```
