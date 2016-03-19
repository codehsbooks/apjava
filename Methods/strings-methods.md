# Strings Methods

You will remember that Strings are a sequence of characters. Let's look at this example String below:

```
String str = "Hello World"
```

Here is a way to think about this String as a sequence of individual characters:

| 0  | 1  | 2  | 3  | 4  | 5  | 6  | 7  | 8  | 9  | 10 |
| -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| H  | e  | l  | l  | o  |    | W  | o  | r  | l  | d  |

Each character in this string has a position from 0 to 10. For example, the first character, `'H'`, is at position 0. The second character, `'e'`, is at position 1. The last character, `'d'`, is at position 10. You will note that the space between the two words, `' '`, is also a character and is located at position 5.

## String Review

Let's review some key points about Strings:

* Strings are **objects**.
* Strings are **not** primitive types (like `char`, `int`, `boolean`, `double`, etc.).
* A **S**tring starts with a capital letter whereas primitive types are all lowercase.
* Since Strings are objects, we must use the `.equals()` method to determine if two Strings are exactly the same. Using `==` to compare two Strings will result in buggy programs.
  * `string1.equals(string2)` **is** the correct way to compare two Strings. `string1 == string2` is **NOT** the correct way to compare two Strings.

## Notes About The Java Documentation

* **The Java Documentation** is the reference for how to use different methods and classes. 
  * [The full Java documentation for all methods and classes is located here](https://docs.oracle.com/javase/7/docs/api/). 
* In this chapter, we will be focusing specifically on the documentation for Strings ([located on this page](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html)).
* Tip: you can find a specific page in the documentation using a search engine like Google. When searching for a specific method or class, search using the keywords "Java  [method or class]". 
  * [For example, here is a Google search for the Java String Documentation](https://www.google.com/search?q=java+string).
  * This is often easier than navigating through the full Java Documentation website.

## String Methods

[If you go to the String documentation page](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html), you will notice that there are ***a lot*** of different methods we can use on Strings. In this section, we will be focusing on some of the key methods from that page which are listed in the table below:

![String Methods Table](../static/methods/string-methods-table.png)

The *left-most column* in the table shows us the return type of the method. The *middle column* in the table shows us the **method signature**. The method signature includes the name of the method and its parameters. The middle column also tells us what the method does. The *right-most* column gives an example of using the method.

### Using The charAt Method

[Todo]

### Using The substring Method

[Todo]

#### Strings Are Immutable:

[Todo]

## Looping Over A String

[Todo]





