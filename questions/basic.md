# Basic Java Interview Questions


+ [1. Explain the System.out.print()](#1-explain-the-systemoutprint)
+ [2. What is the main method and how its works?](#2-what-is-the-main-method-and-how-its-work)
+ [3. What are the access modifiers?](#3-what-are-the-access-modifiers)
+ [4. What is the difference between final, finalize and finally?](#4-what-is-the-difference-between-final-finalize-and-finally)
+ [5. What is the difference between Sting, StringBuilder and StringBuffer?](#5-what-is-the-difference-between-sting-stringbuilder-and-stringbuffer)
+ [6. What is the String Pool in Java?](#6-what-is-the-string-pool-in-java)
+ [7. What is the difference between instance variables and local variables in Java?](#7-what-is-the-difference-between-instance-variables-and-local-variables-in-java)
+ [8. What does 'static' mean in Java?](#8-what-does-static-mean-in-java)
+ [9. What is Exception Handling in Java, and what are the different types of exceptions?](#9-what-is-exception-handling-in-java-and-what-are-the-different-types-of-exceptions)
+ [10. How does Garbage Collection work?](#10-how-does-garbage-collection-work)
+ [11. What are the differences between JDK, JVM, and JRE?](#11-what-are-the-differences-between-jdk-jvm-and-jre)
+ [12. What do Overloading and Overriding mean in Java?](#12-what-do-overloading-and-overriding-mean-in-java)
+ [13. What is the difference between the 'equals' method and the '==' (equality) operator in Java?](#13-what-is-the-difference-between-the-equals-method-and-the-equality-operator-in-java)

## 1. Explain the System.out.print

When you start learning Java, the first thing you will use is `System.out.print` to print some value. However, in interview questions, if they ask you about this, the first thing you will think is, "Okay, I use this to print something, but I don't know how this works." That's what I used to think before in some of the interviews that I had. The interviewer wants to know if you understand the basics of classes, objects, and methods.

Let's break it down step by step. First, we have three components: `System`, `out`, and `print`.

- `System`: The first letter is capitalized, which means in Java, you should know that any class should start with a capital letter. So you will say that `System` is a class that contains fields, objects, and methods.
- `out`: We call `out` in the `System` class, so maybe `out` is a field, object, or method. However, since we are calling `print` after `out`, `out` should be an object. So, `out` is a `PrintStream` object.
- `print`: Here, we pass a value to print something, so it should be a method that accepts argument parameters. Therefore, `print` is a method inside the `out` object used to print values.


## 2. What is the main method and how its work?

main method in Java is the entry point of any standalone Java application

```java
 public static void main(String[] args) {
       System.out.print("Hello World");
   }
```

**The interviewer wants to know about some concepts here:**

1. Access modifier
2. Static keyword
3. Return types of methods
4. Argument parameters

We will delve into each of these concepts one by one in the following questions. Let is start answering the interviewer:

- `public:` It is one of the access modifiers, and it means anyone can access this method.

- `static:` This is a keyword in Java. When we use it with a method, it means we can call this method without creating an object from the class. In other words, it belongs to the class itself.

- `void:` This means that the method doesn't provide any information when it's called.

- `main:` This is the name of the method and serves as the starting point of a Java program.

- `String[] args:` This is a way to provide information to the program when you run it using the command line. It's like a list of words (strings) you can use.


## 3. What are the access modifiers?

`default:` access modifier is without any access specifier. Data members, classes, and methods marked as default are accessible only within the same package.

`private:` access modifiers are marked with the keyword private and are accessible only within the class itself. They are not accessible by classes from the same package.

`protected:` access modifiers can be accessed within the same package or by subclasses from different packages.

`public:` access modifiers are accessible from everywhere.


## 4. What is the difference between Final, Finalize, and Finally?
`final:` is a keyword used in Java to indicate that a variable, method, or class cannot be changed or extended.
- When applied to a variable, it means the variable's value cannot be modified after initialization.
- When applied to a method, it means the method cannot be overridden in subclasses.
- When applied to a class, it means the class cannot be extended by other classes.

`finalize:` is a method in the Object class in Java.
It is called by the garbage collector before reclaiming an object's memory.
You can override the finalize method in your class to provide custom cleanup operations before an object is garbage collected.

`finally:` is a block used in exception handling in Java (try-catch-finally).
The finally block is used to ensure that a certain block of code is always executed, whether an exception is thrown or not.
It is typically used for cleanup operations, like closing files or releasing resources, to ensure they are performed regardless of exceptions.


## What is the difference between Sting, StringBuilder and StringBuffer?

- `String :`
    - Immutable: Once created, the value cannot be changed.
    - Every modification creates a new `String` object.
    - Inefficient for frequent modifications due to memory and performance overhead.
    - Memory: Stored in the String Pool, a special area of the heap memory.
-  `StringBuilder :`
    - Mutable: Allows changes without creating new objects.
    - Not thread-safe: Cannot be safely used in a multi-threaded environment without external synchronization.
    - Efficient for frequent modifications in single-threaded scenarios.
    - Memory: Stored in the heap memory, but not in the String Pool.
- `StringBuffer :`
    - Mutable: Like `StringBuilder`, it allows changes without creating new objects.
    - Thread-safe: Methods are synchronized, making it safe for use in multi-threaded environments.
    - Slightly less efficient than `StringBuilder` due to overhead of synchronization.
    - Memory: Stored in the heap memory, but not in the String Pool.

## 6. What is the String Pool in Java?

- **String Pool**:
    - Special memory region where Java stores literal string values.
    - Optimizes memory usage by storing identical strings in the same location.
    - Strings in the pool are immutable.
    - Achieves memory efficiency by allowing string reuse.

## 7. What is the difference between instance variables and local variables in Java?

- **Instance Variables**:
    - Declared within a class but outside any method.
    - Represents object state; accessible by all methods in the class.
    - Have default values; exist as long as the object exists.
- **Local Variables**:
    - Declared within methods; accessible only there.
    - No default values; must be initialized before use.
    - Exist only during method execution; destroyed afterwards.

## 8. What does 'static' mean in Java?

- **Static**:
    - Indicates class-level members (variables or methods).
    - Accessible without creating a class instance.
    - Shared among all instances of the class.
    - Useful for constants or utility functions.

## 9. What is Exception Handling in Java, and what are the different types of exceptions?

- **Exception Handling**:
    - Mechanism to handle runtime errors, maintaining normal application flow.
    - Uses try-catch blocks.
- **Types of Exceptions**:
    - **Checked Exceptions**: Checked at compile-time (e.g., `IOException`).
    - **Unchecked Exceptions**: Checked at runtime (e.g., `NullPointerException`).

## 10. How does Garbage Collection work?

- **Garbage Collection**:
    - JVM process reclaiming memory from unused objects.
    - Identifies and frees memory of objects no longer in use.
    - Automatic process, prevents memory leaks and optimizes memory.

## 11. What are the differences between JDK, JVM, and JRE?

- **JDK (Java Development Kit)**:
    - Full suite for Java development, including JRE and development tools.
- **JVM (Java Virtual Machine)**:
    - Runs Java bytecode; language-agnostic virtual machine.
- **JRE (Java Runtime Environment)**:
    - Contains JVM and libraries for running Java programs.

## 12. What do Overloading and Overriding mean in Java?

- **Overloading**:
    - Multiple methods with the same name but different parameters in a class.
- **Overriding**:
    - Subclass method providing a specific implementation of a superclass method.

## 13. What is the difference between the 'equals' method and the '==' (equality) operator in Java?

- **'equals' Method**:
    - Checks content equality between objects.
    - Can be overridden in custom classes.
- **'==' Operator**:
    - Checks reference equality (whether two references point to the same object).    