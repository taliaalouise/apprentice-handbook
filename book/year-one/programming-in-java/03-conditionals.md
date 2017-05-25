# Conditional Statements

Conditional statements allow the computer to execute some code **only if a certain condition is true**. This is incredibly important for programming, as it combines with loops to allow the program to make decisions. The main types of conditional statements are the family of `if`, `else if`, and `else`, and the `switch` statement.

## If statements

If statements execute a piece of code *if* a certain condition is true (conditions are anything which can resolve to a `boolean` value). Otherwise, they skip it. They are written:

```java
if (condition) {
    // code you want to run
}
```

If `condition` is true, the code will run, if not, it won't.

### Else If statements

An `else if` statement is tacked onto the end of an `if` statement, written as follows:

```java
if (condition1) {
    // some code
} else if (condition2) {
    // some other code
} else if (condition 3) {
    // yet more code
}
```

The code in an `else if` statement will execute if condition 1 is **NOT** true, but condition 2 **IS**. You can put as many `else if` statements in a row as you like, and each will only execute if all the conditions above them are false, but they are true.

### Else statements

An `else` statement is put after an `if` or `else if` statement, and will automatically run if none of the conditions above it are true. For example:

```java
if (condition1) {
    // code
} else if (condition 2) {
    // more code
} else if (condition 3) {
    // different code
} else {
    // yet more code
}
```

If `condition1` is true, `// code` will execute. If `condition1` is false but `condition2` is true, `// more code` will execute. If `condition1` and `condition2` are false but `condition3` is true, `// different code`. Finally, if none of the conditions are true, `// yet more code` will execute.

## Switch statement

A switch statement is used when the alternative would be making a really long series of `if, else if, else if, else if` etc statements. It works by looking at a variable, usually an `int`, and checking its value against different expected values. It is written like this:

```java
switch (variable) {
    case 1:
        // some code
        break;
    case 2:
        // other code
        break;
    case 3:
        // more code
        break;
    case 4:
        // extra code
        break;
    default:
        // possibly code?
        break;
}
```

If `variable` is equal to one, `// some code` will execute. If `variable` is equal to two, `// other code` will execute, and so on. If `variable` is not equal to any of the `case`s, the `default` case will execute.

**note:** remember the `break;`s! If you leave them out the code will continue to execute and you'll end up running all the code in the statement.

**note:** `variable` can be a string too, in which case you'll want to write stuff like `case "*":`, `case "/":`, `case "+":` and `case "-":`
