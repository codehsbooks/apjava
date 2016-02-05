# Javadocs and More Methods

Javadoc is all about commenting your code correctly. Javadoc is both the tool and the style of commenting your Java programs. Commenting is very important, as it provides notes in our code to help others understand it.


## Javadoc Rules

Javadoc comments are similar to multiline comments, but contain an extra `*`. Here is an example of how Javadoc comments start and end:

``` Java
/**
 * Description of method
 *
 * @param paramName1  description
 * @param paramName2  description
 * return  Description of return value
 */
```

## More Examples

Here are some examples of proper Javadoc comments:

``` Java
 /**
  * This method returns the product of two integers.
  *
  * @param numOne  The first integer
  * @param numTwo  The second integer
  * @return  The product of the two integers
  */
 private int product(int numOne, int numTwo)
 {
    return numOne * numTwo;
 }
 
 /**
  * This method returns an array with each word from a string in it.
  *
  * @param input  The string we want to split.
  * @return  The new string array.
  */
  private String[] split(string input)
  {
    return input.split("\\s+");
  }
```
