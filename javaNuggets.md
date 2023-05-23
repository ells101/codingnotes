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
- There's a shorthand for/each looping over an array. You can use an enhanced for loop as such:

```java
> for (type var : array) # type is the data type of array elements. Var is the variable that holds each element of the array in turn.
```

Java Fundamentals Notes
-----------------------

- **Strings** are only defined by double quotes "" , single quotes '' are for **chars** only.
- Arrays are fixed type. List for when you need to add or remove elements dynamically or when you need to store elements of different types.
- For OOP a rule of thumb would be: instance variables are private and methods should be public.

Math
-----

- `Math.ceil(n)` returns highest rounded number.
- `Math.pow(base, exponent)` returns a (double) result of raising base to power of exponent.
- `Math.min(n, n2)` returns lowest of two integers.

Bitwise
------

- `<<` is the left shift bitwise operators. It shifts a binary representation a specified number of places. e.g.

```java
int value = 5;  // Binary: 00000101
int shifted = value << 2;
// returns 00010100 or 20 in binary code
```

In this example, value is initially set to 5, which has a binary representation of 00000101. The left shift operation value `<< 2` shifts the bits of value two positions to the left. The result will be 00010100, which is equivalent to the decimal value 20.

String
------

- `.repeat` is a new method you can use in Java 11+ to repeat a string 'n' number of times. Syntax = string.repeat(repeatCount).
- `.equals` is used to check the content of another String.
- `.substring()` used to get chars from a String
- `.substring(str.length(-1))` get the last character from of the String.
- `.charAt(n)` gives you the char at a specified `n` index of a String.
- `.startsWith()` lets you check the very first character of a String.
- `String.valueOf` a static method of string class. Used to take one type like an integer and transform it to it's string literal. e.g.

```java
boolean moo = true;
System.out.println(String.valueOf(moo))
// prints out "true"
```

- `.indexOf` searches for first occurrence of a specified substring within the String. e.g.

```java
String yo = "Hello world";
return yo.indexOf("world"); // returns 6
```

StringBuilder
-------

- *Stringbuilder* creates a mutable String that has methods to manipulate the string.
- .append

Maps
-----

- .computeIfPresent() allows you to update a value associated with a key, if the key is present in the map. A lambda expression. It's a 'bifunction' that takes two arguments and returns a result. For example:

```java
    map.computeIfPresent("spinach", (key, value) -> "nuts");
```

This checks if map has the key "spinach". If it does, then update key "spinach" to have value "nuts".

Exception Handling
----------

- Get into the habit of handling, null, empty or sometimes 0 so that your code solutions are more watertight.
- Objects.requireNonNull checks if an object reference is null and throws a null exception if it is. So we can check if a method param is not null.

```java

public void doSomething(String hello)
    Objects.requireNonNull(hello, "hello cannot be of type null");
    //code to do something thereafter.

```

- We can use IllegalArgumentException, it is an unchecked exception which is great when notifying that we should use only one particular data type.

```java
throw new IllegalArgumentException("you should only enter the required type")
```

Streams
--------

- Introduced in Java 8.

Collections Interface
---------

- Sets are great for ensuring no duplicates. It's a collection of unique elements.
- A TreeSet puts characters in natural order and gets rid of duplicate values. Perfect for that kata where you need take two strings and return one string with all unique chars.

SpringBoot
-----

- `@Value` annotation used to inject values from external config files, sys properties, or environment variables into your application. Values usually stored in an `application.properties` file.
- `@Autowired` annotation used to inject dependencies into corresponding fields of the class. e.g. in SpringBoot example `CollegeStudent` and `StudentGrades`. You don't have to manually create instances of these objects, Spring Boot automatically creates and injects them at runtime.
- `ReflectionTestUtils`, allows you to get/set non-public fields directly. Why not just make it public?
  - To be able to test methods/modules which are private and can't be made public. (e.g. You are working at a company and want to create a test but you don't want to change the existing code's access modifier).
- Reflection can be very useful when testing legacy code or dealing with third-party libraries that rely on reflection.
