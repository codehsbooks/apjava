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

## Examples of Recursion
<hr>
Some common examples of recursive solutions include Factorials and the Fibonacci Sequence. Other examples of recursive solutions include: Golden Ratio, Catalan Numbers, and Computer Compound Interest.

#### Factorials and Recursion
One common way to solve for factorials use to use a for loop.
Here is one example:

```Java
private int factorial(int num)
{
  int res = 1;
  for(int i = num; i > 0; i--)
  {
    res *= i;
  }
  return res;
}
```
While this solution definitely works, we can simply it using recursion.
Looking at the formula for factorials: $$n*(n-1)*(n-2)*(n-3)...$$
we can see a recurrence relation of: $$n! =\begin{cases}1 & n = 0,\\(n-1)!*n & n > 0\end{cases}$$ 
<br>

Looking at this from a programming point of view, this means:
``factorial(0);`` equals ``1``, and ``factorial(n);`` equals ``n * factorial(n-1);``

##### Base Case:
Since ``factorial(0);`` is the simplest form we can achieve, it is our base case. This means we want to keep calling our ``factorial();`` method until the input is equal to ``0``.

##### Recursive Case:

#### Fibonacci Sequence and Recursion



## The Humor of Recursion
<hr>
Sometimes recursion is used as the subject of humor for mathematicians and computer scientists. One of the most famed example of humorous recursion can be seen by going to Google and searching: "recursion." 
<br>
<-- include .gif -->