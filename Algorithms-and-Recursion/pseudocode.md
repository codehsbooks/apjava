# Pseudocode

Pseudocode is a brief explanation of code in plain English.

Writing pseudocode is a good way to map out your ideas for a program before actually writing the real code. It can help you think about the function decomposition, the top down design, and the structure of a program.

Here are some examples of pseudocode:

- Pseudocode to put down 10 tennis balls

  ```
  repeat 10 times:
      put ball
  ```
    
- Pseudocode to draw a tower on every avenue in a Karel world.

  ```
  while front is clear:
      build tower
      move
  build last tower
  ```

- Then, you can also pseudocode the build tower part like this:

  ```
  build tower:
      turn left
      repeat 3 times:
          put ball and move
      turn around
      move down
      turn left
  ```

Writing out algorithms in pseudocode allows you to focus on the structure and important ideas of the program without worrying about syntax. Once you have a good idea of the program written in pseudocode, writing the actual program is simply a matter of turning the pseudocode into Java code.
