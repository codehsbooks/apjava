# Advanced: Recursion
<hr>
Recursion is when you break down a given problem into smaller problems of the same instance. The goal is to get the problems into such a small form that they become easy to solve. 

In Computer Science, recursion is when a method calls itself to solve a given problem.

## What Recursion Looks Like
<hr>

![Recursion Example](../static/algorithms/Algorithms_Recursion_Example.jpg)
(Source: https://prateekvjoshi.com/2013/10/05/understanding-recursion-part-i/)

Recursion is such an important part of Computer Science, because it allows us to condense our code into a simple form.

## Parts of a Recursive Method
<hr>

##### Base Case
The ***Base Case*** is the terminating case in a recursive problem. This case does not use recursion, because it is the simplest form of the problem and cases the method to end. If we don't have a ***Base Case*** the recursive method would continue infinitely. 

##### Recursive Case
The ***Recursive Case*** is the set of steps that reduces all the other cases as the ***Recursive Algorithm*** gets closer to the ***Base Case***.

##### Recursive Algorithm
The ***Recursive Algorithm*** is a finite set of steps that calls itself with simpler inputs, as the ***Recursive Case*** approaches the ***Base Case***.

## The Humor of Recursion
<hr>
Sometimes recursion is used as the subject of humor for mathematicians and computer scientists. One of the most famed example of humorous recursion can be seen by going to Google and searching: "recursion." 
<-- include .gif -->