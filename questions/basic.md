These questions you will be asked for any java interview, if you asked question that not in the list feel free to make pull request to this file 

# Basic Java Interview Questions

+ [1. Explain the System.out.print()](#1-explain-the-systemoutprint)
+ [2. What is the main method and how does it work?](#2-what-is-the-main-method-and-how-does-it-work)
+ [3. What are the access modifiers?](#3-what-are-the-access-modifiers)
+ [4. What is the difference between final, finalize, and finally?](#4-what-is-the-difference-between-final-finalize-and-finally)
+ [5. What is the difference between String, StringBuilder, and StringBuffer?](#5-what-is-the-difference-between-string-stringbuilder-and-stringbuffer)
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

## 2. What is the main method and how does it work?

The main method in Java serves as the entry point for any standalone Java application. It's signature is:

```java
public static void main(String[] args) {
    // Your code here
}
```

**The interviewer wants to know about some concepts here:**

1. Access modifier
2. Static keyword
3. Return types of methods
4. Argument parameters

- `public`: An access modifier allowing the method to be accessible from anywhere.
- `static`: Indicates that the method belongs to the class and not a specific instance.
- `void`: Return type indicating the method doesn't return any value.
- `main`: The method name recognized by the JVM as the program's starting point.
- `String[] args`: Parameters for command-line arguments.

## 3. What are the access modifiers?

Access modifiers in Java define the scope of access for classes, methods, and variables. They include:

- `default`: No explicit modifier; accessible within the same package.
- `private`: Accessible only within the declared class.
- `protected`: Accessible within the same package or subclasses in different packages.
- `public`: Accessible from any class.

## 4. What is the difference between final, finalize, and finally?

Yeah this is a tricky question from the interviewer,

- `final`: A keyword used to declare constants or prevent method overriding or inheritance.
  - `final variable:` If you make any variable as final, you cannot change the value of final variable(It will be constant)
  - `final method:` If you make any method as final, you cannot override it.
  - `final class:` If you make any class as final, you cannot extend it.
- `finalize`: A method in the Object class for cleanup before garbage collection.
- `finally`: A block in try-catch-finally for code that executes regardless of exceptions.

## 5. What is the difference between String, StringBuilder, and StringBuffer?

- `String`:
  - Immutable: Value cannot be changed after creation
  - Stored in the String Pool for memory efficiency.
- `StringBuilder`:
  - Mutable: Can be modified without creating new objects.
  - Not thread-safe but efficient in single-threaded scenarios.
- `StringBuffer`:
  - Mutable like StringBuilder but thread-safe.
  - Slightly less efficient due to synchronization.

## 6. What is the String Pool in Java?

The String Pool is a memory region for storing unique string literals. Java optimizes memory by reusing strings from this pool, enhancing performance for string manipulation.

## 7. What is the difference between instance variables and local variables in Java?

- `Instance Variables`: Attributes of an object, accessible throughout the

class.

- `Local Variables`: Declared inside methods, accessible only within the method scope.

## 8. What does 'static' mean in Java?

`static` in Java indicates that a field or method belongs to the class itself rather than an instance, allowing direct access without creating an object.

## 9. What is Exception Handling in Java, and what are the different types of exceptions?

Certainly! Here's an improved explanation of Exception Handling in Java, with clearer points and examples for each type of exception:

## 9. What is Exception Handling in Java, and what are the different types of exceptions?

Exception Handling in Java is a method to manage runtime errors, ensuring that the flow of the program does not break when an unexpected event occurs. It primarily uses `try-catch` blocks. There are two main types of exceptions in Java:

- **Checked Exceptions**:
  - These are exceptions that are checked at compile-time.
  - The compiler requires these exceptions to be caught or declared in the method signature.
  - Example: `IOException`, which occurs when an input/output operation fails or is interrupted.
  - Code example:
      ```java
      try {
          FileInputStream file = new FileInputStream("somefile.txt");
          // Use file
      } catch (IOException e) {
          // Handle exception
      }
      ```

- **Unchecked Exceptions**:
  - These exceptions are not checked at compile-time, meaning the compiler does not force the programmer to handle or declare these exceptions.
  - They usually indicate programming bugs, such as logic errors or improper use of an API.
  - Example: `NullPointerException`, which occurs when you try to use a reference that points to no location in memory.
  - Code example:
      ```java
      String text = null;
      try {
          System.out.println(text.length());
      } catch (NullPointerException e) {
          // Handle exception
      }
      ```

## 10. How does Garbage Collection work?

Garbage Collection (GC) in Java is a process that automatically identifies and frees memory that is no longer in use by the program. It is a critical part of Java's memory management system and plays a vital role in resource management and performance optimization.

#### Why Does Java Need Garbage Collection?
- **Memory Efficiency**: Without GC, objects that are no longer needed would still occupy memory space, leading to inefficient memory usage.
- **Performance Optimization**: Proper memory management ensures that applications run smoothly, without memory leaks that can degrade performance.- 
- **Programmer Convenience**: Manual memory management is prone to errors. GC automates this process, reducing the likelihood of issues like memory leaks and dangling pointers.

#### Who Manages Garbage Collection?

The Java Virtual Machine (JVM) manages Garbage Collection. It has a garbage collector that periodically executes to free up memory space.

#### How Does Garbage Collection Work?
- **Identifying Garbage**: Objects that are no longer reachable, meaning no part of your program maintains a reference to them, are considered garbage.
- **Reclaiming Memory**: The garbage collector reclaims the memory allocated to these unreachable objects and returns it to the memory pool.

#### What Happens If There Is No Garbage Collection?

- The burden of memory management falls on the programmer, increasing the complexity of the code.
- There is a higher risk of memory leaks, where unused objects continue to occupy memory, leading to inefficiency and, in severe cases, application crashes.
- The application may suffer from increased memory usage and reduced performance over time.

## 11. What are the differences between JDK, JVM, and JRE?

- `JDK`: Java Development Kit, the complete kit for developing Java applications.
- `JVM`: Java Virtual Machine, executes Java bytecode and provides a runtime environment.
- `JRE`: Java Runtime Environment, consists of JVM and core libraries for running Java applications.

## 12. What do Overloading and Overriding mean in Java?

Overloading and Overriding are two concepts that allow you to define methods with the same name but different functionalities.

### Overloading
- **Definition**: Occurs when two or more methods in a class have the same name but different parameters (different type, number, or both).
- **Example**:
    ```java
    class ExampleClass {
        // Overloaded method with one parameter
        void display(int a) {
            System.out.println("Got Integer data.");
        }

        // Overloaded method with different parameter
        void display(String a) {
            System.out.println("Got String data.");
        }
    }
    ```

### Overriding
- **Definition**: When a method in a subclass has the same name, return type, and parameters as a method in its superclass, thereby providing its own implementation.
- **Example**:
    ```java
    class ParentClass {
        void show() {
            System.out.println("Parent show method");
        }
    }

    class ChildClass extends ParentClass {
        // Overriding method
        @Override
        void show() {
            System.out.println("Child show method");
        }
    }
    ```

### True/False Examples

1. **Overloading Example**:
    ```java
    class Demo {
        void foo(int a) { /*...*/ }
        void foo(int a, int b) { /*...*/ } 
       // True: This is a valid example of overloading.
    }

    class Demo {
        int foo(int a) { return a; }
        double foo(int a) { return 2.5; }
       // False: Overloading cannot be done by changing the return type alone.
    }
    ```

2. **Overriding Example**:
    ```java
    class A {
        void display() { System.out.println("A"); }
    }
    class B extends A {
        @Override
        void display() { System.out.println("B"); }
       // True: This is a valid example of overriding.
    }

    class A {
        void display() { System.out.println("A"); }
    }
    class B extends A {
        int display() { return 1; } 
      // False: Overriding cannot change the return type if it changes the method signature.
    }
    ``` 

## 13. What is the difference between the equals method and the equality operator in java?

- `'equals'`: A method for checking content equality between objects.
- `'=='`: An operator for checking reference equality between objects.

#### 'equals' Method
- **Usage**: It's a method defined in the `Object` class for checking content equality between two objects.
- **Functionality**: It compares the values inside the objects. The method can be overridden in a class to define what equality means for instances of that class.
- **Example**:
    ```java
    String str1 = new String("Hello");
    String str2 = new String("Hello");
    boolean result = str1.equals(str2); // True, because the content is the same.
    ```

#### '==' Operator
- **Usage**: An operator that checks if two references point to the same object.
- **Functionality**: It compares the memory addresses of the objects, not their content.
- **Example**:
    ```java
    String str1 = new String("Hello");
    String str2 = new String("Hello");
    boolean result = str1 == str2; // False, because they are two different objects in memory.
    ```

#### When I can use them ?
- Use `'equals'` when you want to compare the contents or values of objects.
- Use `'=='` when you want to know if two references are pointing to the same object in memory.
