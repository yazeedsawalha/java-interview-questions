# Basic Java Interview Questions


+ [1. Explain the System.out.print()](#1-explain-the-systemoutprint)
+ [2. What is the main method and how its works?](#2-what-is-the-main-method-and-how-its-work)
+ [3. What are the access modifiers?](#3-what-are-the-access-modifiers)
+ [4. What is the difference between Final, Finalize and Finally?](#4-what-is-the-difference-between-final-finalize-and-finally)
  

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
