# Logical Operators

## What Are Logical Operators?

Boolean variables can only take on one of two possible values, true or false. Logical operators allow you to combine and connect booleans in useful ways.

There are three fundamental boolean operators:

- NOT
- OR
- AND

These should look quite familiar; in fact, we use them in speech every day! The NOT operator is used on a single boolean, wheres AND and OR are used across multiple boolean values.

## The NOT Operator

NOT is represented in JavaScript as `!`. When placed in front of a boolean value, NOT causes the boolean to take on its opposite value. For example "NOT true" gives the answer "false." This is fairly intuitive -- if something is not true, then it must be false. Similarly, if something is not false, then it must be true.

The example below sets up a variable `hungry` as being true. Then it prints out NOT `hungry`.

```
boolean hungry = true;
System.out.println(!hungry);   // prints "false"
```

For a variable `p` that can be `true` or `false`:

| p     | !p    |
|-------|-------|
| true  | false |
| false | true  |


## The AND Operator

AND is represent in JavaScript as: &&. An expression using AND is true only when all its component parts are true. If any of the boolean values are false, the whole expression evaluates to false.

For example, if it is 6:30am AND it is a school day, you should wake up. You can test the expression of "6:30am AND a school day." If both are true, then the whole expression evaluates to true. If either or both are false, then the whole expression is false, and you should stay in bed.

```
boolean sixThirty = true;
boolean schoolDay = false;
System.out.println(sixThirty && schoolDay);  // because both values aren't true, it prints "false"
```

For variables `p` and `q` that can be `true` or `false`:

| p     | q     |   | p AND q |
|-------|-------|---|--------|
| true  | true  |   | true   |
| true  | false |   | false  |
| false | true  |   | false  |
| false | false |   | false  |


## The OR Operator

OR is represented in JavaScript as `||`. An expression using OR is true when all or any of its parts are true. It is only false when all of the boolean values are false.

Say that you are trying to decide whether to wear a coat today. You'll wear your coat if it is raining right now or if it is cold outside. You can evaluate this expression based on the answers to those two boolean values. If it's raining, cold, or raining and cold, then you will wear your coat. The only case in which you would not wear your coat is if it's neither raining nor cold.

```
boolean isRaining = true;
boolean isCold = false;
System.out.println(isRaining || isCold);  // it's not cold, but it is raining, so it prints true
```

For variables `p` and `q` that can be `true` or `false`:

| p     | q     |   | p OR q |
|-------|-------|---|--------|
| true  | true  |   | true   |
| true  | false |   | true   |
| false | true  |   | true   |
| false | false |   | false  |
