# String Processing

In this chapter, we will combine everything we have learned about Strings and characters so far. You will become more familiar with the underlying patterns involved in processing Strings. By using these patterns, you will learn how to do more advanced forms of **String processing**.

## String Processing Pseudocode

**Pseudocode** is a step-by-step description of what you want a program to do in plain English. Before writing any actual code, it is always recommended you write pseudocode first. This helps us figure out how to structure more complex programs without getting bogged down in specifics. 

By now, you should be familiar with how to loop over Strings. Looping over Strings is the most common form of **String processing**. You will consistently find yourself having to write methods which do something to each of the characters in a String. This follows a pattern, and that pattern can be expressed in the pseudocode given below:

```
Create a result String
For every character in the String
    Do something with the current character
Return your result
```

We can use this as a guideline to write many different types of String processing methods. Take this as an example:

```
private String processAStringExample(String str){
    String resultingString = ""; // Create a result String
    for(int i = 0; i < str.length(); i++) // For every character in the String
    {
        resultingString += str.charAt(i); // Do something with the current character
    }
    return resultingString; // Return your result
}
```

The relevant pseudocode for each line of actual code is given on the right. Let's test our method to make sure it works:

```
public class Palindromes extends ConsoleProgram
{
    /**
     * This program lets the user input some text and
     * prints out whether or not that text is a palindrome.
     */
    public void run()
    {
        String str = readLine("Enter a String for processing: ");
        System.out.println("You typed: " + processAStringExample(str));
    }
    
    private String processAStringExample(String str){
        String resultingString = ""; // Create a result String
        for(int i = 0; i < str.length(); i++) // For every character in the String
        {
            resultingString += str.charAt(i); // Do something with the current character
        }
        return resultingString; // Return your result
    }
}
```

We have added a run method to test String input from the user. Here is an example of what a user might type as a test String after running the program:

```
Enter a String for processing: Process this String!
You typed: Process this String!
```

You are not limited to simply storing each character into a new resulting String. You can do anything to each of the characters. You could change the case, change the ordering, or even change each of the characters into a different character entirely. The possibilities are endless with how you choose to process the String!

## Finding Palindromes

Let's look at a more advanced example of String processing. In this example, we will write a program which checks to see if a given String is a palindrome. **A palindrome** is a word or sentence that is the same forwards and backwards. Here are a some examples of palindromes:

```
racecar
mom
A man, a plan, a canal - Panama!
```

### Writing an `isPalindrome` Method

Let's use **top-down design** and **pseudocode** to help us solve this problem. In order for a String to be a palindrome, we know that it must:

* Be the same forwards and backwards.
* Be equal to the reversed version of the String.

Let's write a method in pseudocode which checks for this:

```
isPalindrome(String text)
    reversed = get reversed text
    if text is equal to reversed
        return true
    return false
```

First, we want to reverse the String, so we will have to write another method to do that. Then, if the original String is equal to the reversed String, we know that it must be a palindrome. Our method will return true. If the original String is **not** equal to the reversed String, we know that it is not a palindrome. Our method returns false instead.

### Writing a `reverse` Method

Now that we know we need a reverse method, we can write the pseudocode for that:

```
reverse(String text)
    result = "";
    for every character starting from the end
        add it to result
    return result
```

Does this look familiar? It should! We are using the same general pattern for processing a String that was given at the start of this chapter!

First, we need to create a result String. We then take a look at each character *starting from the end of the String*. We add each of these characters into the result String. We finish by returning the resulting reversed String.

### Putting It All Together

With both methods written in pseudocode, we have a good outline for our program:

```
public class Palindromes extends ConsoleProgram
{
    // Let's write a program that determines if a word is a palindrome.
    public void run()
    {
        
    }
    
    isPalindrome(String text)
        reversed = get reversed text
        if text is equal to reversed
            return true
        return false
    
    reverse(String text)
        result = "";
        for every character starting from the end
            add it to result
        return result
}
```

We just need to fill in the details!

```
public class Palindromes extends ConsoleProgram
{
    /**
     * This program lets the user input some text and
     * prints out whether or not that text is a palindrome.
     */
    public void run()
    {
        String text = readLine("Type in your text: ");
        if(isPalindrome(text))
        {
            System.out.println("Your word is a palindrome!");
        }
        else
        {
            System.out.println("Not a palindrome :(");
        }
    }
    
    /**
     * This method determines if a String is a palindrome,
     * which means it is the same forwards and backwards.
     * 
     * @param text The text we want to determine if it is a palindrome.
     * @return A boolean of whether or not it was a palindrome.
     */
    private boolean isPalindrome(String text)
    {
        String reversed = reverse(text);
        if(text.equals(reversed))
        {
            return true;
        }
        else
        {
            return false;
        }
    }
    
    /**
     * This method reverses a String.
     * 
     * @param text The string to reverse.
     * @return The new reversed String.
     */
    private String reverse(String text)
    {
        String result = "";
        for(int i = text.length() - 1; i >= 0; i--)
        {
            char cur = text.charAt(i);
            result += cur;
        }
        return result;
    }
}
```

In our run method, we get a String from the user. We then check to see if it is a palindrome by calling the `isPalindrome` method. Since we have the pseudocode already written for this method, we just need to convert it into actual code. Once we have that method finished, we can do the same for the `reverse` method.

Let's test it with a palindrome!:

```
Type in your text: racecar
Your word is a palindrome!
```

Now let's test it with a word that is **not** a palindrome:

```
Type in your text: CodeHS
Not a palindrome :(
```

By using good top-down design principles and writing out pseudocode for each of our methods, we have created a very advanced String processing program.
