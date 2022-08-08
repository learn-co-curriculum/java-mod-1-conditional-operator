# Conditional Operator

## Learning Goals

- Explain what the conditional operator is

## What is a Conditional Operator?

The **conditional operator** is a ternary operator (takes three operands) that
is used to evaluate a boolean expression. Using this operator could replace an
if-else statement to reduce the number of lines of code written.

The syntax for a conditional operator is as follows:

`variable = (boolean expression) ? value if true : value if false`

To see the conditional operator in action, let us look at this if-else
statement:

```java
String feedback;
if (grade >= 70) {
    feedback = "Congrats! You passed!";
} else {
    feedback = "Oops! Better luck next time!";
}
```

Now let's use the conditional operator instead of the if-else statement:

```java
String feedback = (grade >= 70) ? "Congrats! You passed!" : "Oops! Better luck next time!";
```

Conditional operators have the advantage of condensing multiple lines of code.
It works the same way as the if-else statement as well. If the boolean
expression evaluates to true, it will only evaluate the expression between the
`?` and the `:`. This could be the equivalent to falling into the `if` block.
If the boolean expression evaluates to false, then it will only evaluate the
expression after the `:`.

The conditional operator is great for simple conditional statements! It would
fall short if it was expected to perform more, like nesting. **Nesting** is
when additional conditional statements occur within an `if` block. Let's look
at the example of a nesting if-else statement:

```java
String feedback;
if (grade >= 70) {
    if (grade >= 90) {
        feedback = "Wow! You got an A!";
    } else {
        feedback = "Congrats! You passed!";
    }
} else {
    feedback = "Oops! Better luck next time!";
}
```

Now let us see what this would look like using the ternary conditional operator.

```java
String feedback = (grade >= 70)
    ? ((grade >= 90) ? "Wow! You got an A!" : "Congrats! You passed!")
    : "Oops! Better luck next time!";
```

As we can see, we can definitely convert the nesting if-else statement into a
conditional operator statement; however, the readability of the code isn't as
clear as the if-else statement now. Because of this, it is not recommended to
use nested ternary constructs. The best option at this point would be to create
the nested if-else block.
