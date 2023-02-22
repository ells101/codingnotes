Java Tips
=========

- In java, all code is written within classes. Our program needs to have *at least one* class. e.g in java.hello the class is `Hello`.
- lowerCamelCase for local variables, UpperCamelCase for classes.
- Unlike Javascript or Ruby, a Java file needs first to be compiled to an executable program. e.g
in the hello java example, Hello.class is added to the folder after calling javac. This file is the compiled version of the Java source file.
- When using printf and %f (float) format specifier, to trim trailing zero's simply write: %.1f (for 1 zero) %.2f (for two zeros) etc etc...
- "void" in public static void main (function declaration) means: nothing is expected to be returned in the function. The return result will be
nothing, i.e void.
- Compiling is actually great way of catching errors. A benefit of Java! Code will not compile if there are bugs/errors.
- Primitives and Objects difference? Objects have built-in behaviour. `String` = Object, `int` = primitive.
- The valueOf method is a static method which returns the string representation of the given value. It can be used on primitive types too! Such as 'int', 'boolean' as well as reference types like 'object' and arrays.
- Need to turn an integer into a float or cast any type? You can return like this: *Where result is a double* return (int) result; Using brackets to cast the variable into another allows you to change the variable type. Some precision is lost when converting a double to an integer as the double will be rounded down.
- .repeat is a new method you can use in Java 11+ to repeat a string 'n' number of times. Syntax = string.repeat(repeatCount).
= There's a shorthand for/each looping over an array. You can use

> for (type var : array) # type is the data type of array elements. Var is the variable that holds each element of the array in turn.
> //loop body

Java Fundamentals Notes
-----------------------

- Strings are only defined by double quotes "" , single quotes'' don't work .
= Arrays are fixed type. List for when you need to add or remove elements dynamically or when you need to store elements of different types.
