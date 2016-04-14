# Strings and Characters
Let's review some key differences between Strings and characters:

| Strings | characters |
| -- | -- |
| Type: String | Type: char |
| Object | primitive |
| Compare using the `.equals()` method| Compare using `==` |
| Surrounded by double quotes (Example: "hello") | Surrounded by single quotes (Example: 'a') |
| Sequence of characters (Example: "hello") | A single character (Example: 'a')|

Here is an example of declaring a String in Java:
```
String website = "CodeHS";
```
And here is an example of declaring a character in Java:
```
char letter = 'b';
```

Let's break apart these two examples into their individual components:

![Strings and Characters Declaration Components](../static/methods/strings-and-characters-declaration-components.png)

Highlighted in blue is the type. On the left, we have the type for Strings, `String`. On the right, we have the type for characters, `char`. Highlighted in orange is the name of our variables. We can name them whatever we want, but our names should follow proper naming conventions and make sense. Highlighted in red is the value. This is the actual String and character we are assigning to our variable.

## Characters are Numbers!

Computers prefer working with numbers rather than letters. Thus, every character is actually a unique number behind the scenes. The table below lists each character's assigned number. This table is known as the **ASCII** (***A***merican ***S***tandard ***C***ode for ***I***nformation ***I***nterchange) **table**:

![ASCII Table](../static/methods/ascii-table.jpg)

The table has three columns. The first column, `Hex`, gives us each character as a **hexadecimal number**. Hexadecimal numbers are just another way for us to represent each character, but for now, we will ignore this column. It isn't important to us right now. The second column, `Dec`, gives us each character as a **decimal number**. Decimal numbers are the standard numbers that we are all used to working with (0, 1, 2, 3, 4, etc.). The third column, `Char`, lists each of the corresponding characters.

It is important to remember that lowercase and capital letters are assigned different numbers. For example, the capitalized character 'A' is the number 65 whereas the lowercase character 'a' is the number 97. 

You will also notice that there are a lot of special characters like "NULL" (number 0), "TAB" (number 9), and "CAN" (number 24). Most of these special characters are abbreviated, so they are spelled out more clearly to the right. For example, "CAN" stands for "Cancel". Even things like spaces (number 32), exclamation points (number 33), dollar signs (number 36), and semicolons (number 59) are considered characters!

### Characters as Numbers in a Program

Here is a program that prints out different characters as numbers:

```
public class CharsAreNumbers extends ConsoleProgram
{
    // If you want to see more about the ints behind every
    // char take a full look at the ASCII table
    // You can also find the ASCII table at http://www.asciitable.com/
    public void run()
    {
        // 'a' has the ASCII value 97
        System.out.println("Testing if 'a' has the ASCII value 97:");
        char lowercaseA = 'a';
        System.out.println("'a' as a letter: " + lowercaseA);
        System.out.println("'a' as a number: " + (int)lowercaseA);

        // 'A' has the ASCII value 65
        System.out.println();
        System.out.println("Testing if 'A' has the ASCII value 65:");
        char uppercaseA = 'A';
        System.out.println("'A' as a letter: " + uppercaseA);
        System.out.println("'A' as a number: " + (int)uppercaseA);
        
        // 'j' has the ASCII value 106
        System.out.println();
        System.out.println("Testing if 'j' has the ASCII value 106:");
        char lowercaseJ = 'j';
        System.out.println("'j' as a letter: " + lowercaseJ);
        System.out.println("'j' as a number: " + (int)lowercaseJ);
        
        // 'J' has the ASCII value 74
        System.out.println();
        System.out.println("Testing if 'J' has the ASCII value 74:");
        char uppercaseJ = 'J';
        System.out.println("'J' as a letter: " + uppercaseJ);
        System.out.println("'J' as a number: " + (int)uppercaseJ);
        
        // '!' has the ASCII value 33
        System.out.println();
        System.out.println("Testing if '!' has the ASCII value 33:");
        char exclamationPoint = '!';
        System.out.println("'!' as a character: " + exclamationPoint);
        System.out.println("'!' as a number: " + (int)exclamationPoint);
        
        // '$' has the ASCII value 36
        System.out.println();
        System.out.println("Testing if '$' has the ASCII value 36:");
        char dollarSign = '$';
        System.out.println("'$' as a character: " + dollarSign);
        System.out.println("'$' as a number: " + (int)dollarSign);
    }
}
```

Here we are testing to make sure that each of these characters correspond correctly to their ASCII table numbers. First, we test lowercase and capital letters 'a' and 'A' as well as 'j' and 'J'. Then we test a couple of non-letter characters, the exclamation point ('!') and dollar symbol ('$').  Does it work? Does our output match with the ASCII table above? Let's run the program to check:

```
Testing if 'a' has the ASCII value 97:
'a' as a letter: a
'a' as a number: 97

Testing if 'A' has the ASCII value 65:
'A' as a letter: A
'A' as a number: 65

Testing if 'j' has the ASCII value 106:
'j' as a letter: j
'j' as a number: 106

Testing if 'J' has the ASCII value 74:
'J' as a letter: J
'J' as a number: 74

Testing if '!' has the ASCII value 33:
'!' as a character: !
'!' as a number: 33

Testing if '$' has the ASCII value 36:
'$' as a character: $
'$' as a number: 36
```

Looks good!

#### Adding and Subtracting Characters

Yes! You heard that right. Because characters are numbers, we can add and subtract them. So how does this work? Take a look at the example program below:

```
public class CharsAreNumbers extends ConsoleProgram
{
    // If you want to see more about the ints behind every
    // char take a full look at the ASCII table
    // You can also find the ASCII table at http://www.asciitable.com/
    public void run()
    {
        // 'C' is 2 characters after 'A'
        System.out.println("SUBTRACTING EXAMPLE:");
        System.out.println("'C' as a number: " + (int)'C');
        System.out.println("'A' as a number: " + (int)'A');
        System.out.println("Thus, 'C' is 2 characters after 'A'");
        int difference = 'C' - 'A';
        System.out.println("'C' - 'A' = " + difference);
        
        // 'K' is 10 characters after 'A'
        System.out.println();
        System.out.println("ADDING EXAMPLE:");
        System.out.println("'K' is 10 characters after 'A'");

        char tenAfter = (char)('A' + 10);
        System.out.println("'A' + 10 = " + tenAfter);
        
        System.out.println("How does that work?");

        char capitalA = 'A';
        System.out.println(capitalA);
        System.out.println(".... has the int value ...");
        
        int capitalAInt = (int)capitalA;
        System.out.println(capitalAInt);
        
        System.out.println(".... add 10 and you get ...");
        int capitalAPlusTen = capitalAInt + 10;
        System.out.println(capitalAPlusTen);
        
        System.out.println("... cast that back to a char and you get...");

        char backToChar = (char)capitalAPlusTen;
        System.out.println(backToChar);
    }
}
```


## Escape Sequences

### Escape Sequences in a Program

## The Character Class

### Useful Methods in the Character Class

#### Character Methods Program



