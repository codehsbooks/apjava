# Strings
 As you have learned, a character is one of the primitive data types in Java. We use the `char` keyword to declare it. A character is a single letter. `'A'`, `'a'`, `'D'`, and `'Z'` are all examples of characters. 

It is great that we have an easy way to represent a single character, but what if we wanted to represent words or sentences? How can we do this?

## Introducing Strings

A String is a sequence of characters. We use Strings to represent full words and sentences. For example,  the famous `"Hello World"` is a String. Some more examples of Strings:

* `"I am a String. A sequence of characters strung together to form words and/or sentences."`
* `"CodeHS is the best coding website ever! Everyone loves CodeHS!"`
* `"She sells sea shells by the sea shore."`
* `"Strings!"`
* `"abcdefghijklmnopqrstuvwxyz"`

A String is **not** a primitive type like `int`, `char`, `boolean`, and `double` are. Primitive types always start with lowercase letters, but a **S**tring starts with a capital letter. This makes it an **object**. You will learn more about objects in future chapters, but for now, it is important to just remember that a String is **not** a primitive type.

## Concatenating Strings

Concatenate is a fancy word for joining or linking two things together. To concatenate two or more Strings means that you are joining them together to form one String. We can do this in Java by using the addition operator, `+`.

In this example, we concatenate two separate Strings, "Mc" and "Donalds", to form one String, "McDonalds"

```
public class ConcatenateStrings extends ConsoleProgram
{
    public void run()
    {
        String one = "Mc";
        String two = "Donalds";
        String concatenate = one + two;
        System.out.println(cancatenate);
    }
}
```

After running the program, the concatenated String "McDonalds" gets printed to the screen.

### Concatenating Strings with Primitive Data Types:

We are not limited to concatenating Strings with other Strings. We can concatenate Strings with other data types. Here we are concatenating a String and an integer together: 

```
public class ConcatenateStringAndInt extends ConsoleProgram
{
    public void run()
    {
        int number = 24;
        System.out.println("This String is concatenated with an integer at the end: " + number);
    }
}
```

Look familiar? We have been doing this all the time in previous programs when printing out results to the screen! After running the program, we get:

```
This string is concatenated with an integer at the end: 24
```

You can also concatenate Strings with other primitive types like `char`, `boolean`, and `double`.

## Comparing Strings

In this program, we are comparing two Strings to determine if they are the same. We start by asking the user what the best programming website is. Their answer gets stored into the `programmingWebsite` String variable. We then attempt compare their answer with another String, "CodeHS". If they match, we congratulate them for making the right choice. If they don't match, we inform them that CodeHS is the best.

```
public class ComparingStrings extends ConsoleProgram
{
    public void run()
    {
        String programmingWebsite = readLine("What is the best programming website ever? ");
        if (programmingWebsite == "CodeHS") 
        {
            System.out.println("Absolutely! Everyone loves CodeHS!");
        }
        else 
        {
            System.out.println("No! CodeHS is the best!");
        }
    }
}
```

This should work as we expect, right? Not quite! There is a major bug in our program! If the user types the correct answer to the question after running the program, this happens:

```
What is the best programming website ever? CodeHS
No! CodeHS is the best!
```

So what went wrong? **We can not use `==` to compare Strings since they are not primitive types!** **Instead, we must compare Strings using the `.equals()` method.** This change is shown below:

```
public class ComparingStrings extends ConsoleProgram
{
    public void run()
    {
        String programmingWebsite = readLine("What is the best programming website ever? ");
        if (programmingWebsite.equals("CodeHS")) 
        {
            System.out.println("Absolutely! Everyone loves CodeHS!");
        }
        else 
        {
            System.out.println("No! CodeHS is the best!");
        }
    }
}
```

By removing the `==` and comparing the two Strings with the proper `.equals()` method, our program now works as expected:

```
What is the best programming website ever? CodeHS
Absolutely! Everyone loves CodeHS!
```

Hooray! The bug is now gone!

It is important to note that when we compare Strings, it is case-sensitive. Uppercase and lowercase letters need to match exactly. Typing `codeHS` or `Codehs` as an answer will not work because capitalization matters.

#### Thus, The General Format for Comparing Two Strings Is:

```
boolean result = stringOne.equals(stringTwo);
```
Comparing two Strings will always return a boolean result of either **true** or **false**. The Strings either match or they don't.