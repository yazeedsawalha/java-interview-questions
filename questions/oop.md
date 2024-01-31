These questions you will be asked for any java interview, if you asked question that not in the list feel free to make
pull request to this file

![OOP Interview Questions](../images/questions/oop.png)

# OOP Interview Questions

+ [1. What is Object-Oriented Programming (OOP)?](#1-what-is-object-oriented-programming-oop)
+ [2. What Defines an Object in Object-Oriented Programming?](#2-what-defines-an-object-in-object-oriented-programming)
+ [3. How is a Class Characterized in Object-Oriented Programming?](#3-how-is-a-class-characterized-in-object-oriented-programming)
+ [4. What is an Interface in Object-Oriented Programming?](#4-what-is-an-interface-in-object-oriented-programming)
+ [5. What are the Core Features of Object-Oriented Programming?](#5-what-are-the-core-features-of-object-oriented-programming)
  + [5.1 What is Inheritance in OOP?](#51-what-is-inheritance-in-oop)
  + [5.2 What is Encapsulation in OOP?](#52-what-is-encapsulation-in-oop)
  + [5.3 What is Polymorphism in OOP?](#53-what-is-polymorphism-in-oop)
  + [5.4 What is Abstraction in OOP?](#54-what-is-abstraction-in-oop)
+ [6. How do Interfaces Differ from Abstract Classes in OOP?](#6-how-do-interfaces-differ-from-abstract-classes-in-oop)
+ [7. Does Java Support Multiple Inheritance?](#7-does-java-support-multiple-inheritance)
## 1. What is Object-Oriented Programming (OOP)?

**Interviewer:** Could you explain what Object-Oriented Programming is?

**Interviewee:** Object-Oriented Programming, or OOP, is a programming paradigm that uses "objects" to design software. It's a method of structuring a program by bundling related properties and behaviors into individual units, or objects.

**When to Use:**
OOP is used for modeling complex systems, maintaining code easily, and creating scalable and manageable frameworks. It's ideal for programs with similar actions on different objects and for keeping code flexible and efficient.

**Real-Life Example:**
Consider a car manufacturing company. Each car they produce is an object. These cars share common attributes (like wheels, engines, and seats) and behaviors (like accelerating and braking), but each car can have different values for these attributes and perform behaviors differently.

**Performance Consideration:**
OOP can be less efficient in performance compared to procedural programming, especially in memory usage. However, its benefits in clarity, maintenance, and scalability often outweigh these drawbacks.

**Why Choose OOP:**
Choose OOP for complex applications where modularity, reusability, and flexibility are key. It's great for scenarios with multiple uses of the same class of objects, each with their own state and behavior.

[back to the top](#oop-interview-questions)

---

## 2. What Defines an Object in Object-Oriented Programming?

**Interviewer:** How would you define an object in OOP terms?

**Interviewee:** In OOP, an object is a fundamental unit representing a real-world entity. It's a self-contained block with attributes and methods. Attributes are data stored inside the object (characteristics or properties), and methods are actions an object can perform.

**When to Use:**
Objects are used to model real-world entities in your program. They're ideal for scenarios where encapsulating both data and behaviors in a single unit is beneficial.

**Real-Life Example:**
In a library management system, each book can be an object with attributes like title, author, and ISBN, and methods like borrow and return.

**Performance Consideration:**
Objects can increase overhead, especially in memory-intensive applications, as each object maintains its own data. However, the benefits of using objects often outweigh these costs.

**Why Choose Objects:**
Objects are chosen for their ability to represent complex entities with both data and behavior, making code more intuitive and aligned with real-world scenarios.

[back to the top](#oop-interview-questions)

---

## 3. How is a Class Characterized in Object-Oriented Programming?

**Interviewer:** Can you describe what a class is in the context of OOP?

**Interviewee:** A class in OOP is like a blueprint for creating objects. It defines a data structure that encapsulates data and methods.

**When to Use:**
Classes are used when you need a template for creating multiple objects with similar properties and behaviors.

**Real-Life Example:**
Think of a class as a blueprint for a house. Each house built from this blueprint is an object, with the same structure but potentially different interior designs (attributes).

[back to the top](#oop-interview-questions)

---

## 4. What is an Interface in Object-Oriented Programming?

**Interviewer:** How would you explain an interface in OOP?

**Interviewee:** An interface in OOP is a contract that defines a set of methods that implementing classes must use. It's like a blueprint for what a class should do, without specifying how.

**When to Use:**
Interfaces are used when you want to enforce certain functionalities across different classes.

**Real-Life Example:**
Consider an interface as a checklist for building a house. Different types of houses (classes) can use the same checklist (interface) but implement the details differently.

**Performance Consideration:**
Interfaces do not directly impact performance but are crucial for designing flexible and maintainable code.

**Why Choose Interfaces:**
Interfaces are chosen for their ability to enforce a certain set of methods across multiple classes, promoting consistency and flexibility in large codebases.

[back to the top](#oop-interview-questions)

---

## 5. What are the Core Features of Object-Oriented Programming?

**Interviewer:** Can you list and briefly explain the core features of OOP?

**Interviewee:** Inheritance, Encapsulation, Polymorphism, and Abstraction.

### 5.1 What is Inheritance in OOP?

Inheritance is a mechanism where a new class is derived from an existing class. It's like a child inheriting traits from a parent, allowing for code reusability and the extension of existing code.

**Example**
```java
class A { // Base class
  public void display() {
    System.out.println("Class A display");
  }
}

class B extends A { // Derived class
  public void show() {
    System.out.println("Class B show");
  }
}

public class Main {
  public static void main(String[] args) {
    B obj = new B();
    obj.display(); // Inherited method
    obj.show(); // Own method
  }
}

```
### 5.2 What is Encapsulation in OOP?

Encapsulation is the bundling of data and methods that manipulate that data into a single unit or class, often restricting access to certain components. It's like a capsule, keeping the internal workings safe and hidden.


**Example**
```java
class A {
  private int data; // Encapsulated data

  public void setData(int data) {
    this.data = data; // Setter method
  }

  public int getData() {
    return this.data; // Getter method
  }
}

public class Main {
  public static void main(String[] args) {
    A obj = new A();
    obj.setData(10); // Setting data
    System.out.println(obj.getData()); // Getting data
  }
}

```
### 5.3 What is Polymorphism in OOP?

Polymorphism allows methods to do different things based on the object they are acting upon. It's like speaking different languages (methods) fluently depending on whom you're talking to (the object).
**Example**
```java
class A {
  public void display() {
    System.out.println("Display from Class A");
  }
}

class B extends A {
  public void display() {
    System.out.println("Display from Class B");
  }
}

public class Main {
  public static void main(String[] args) {
    A obj1 = new A();
    A obj2 = new B(); // Polymorphism
    obj1.display(); // Display from Class A
    obj2.display(); // Display from Class B (Overridden method)
  }
}


```
### 5.4 What is Abstraction in OOP?

Abstraction means hiding complex implementation details and showing only the necessary features of an object. It's like a car's steering wheel; you don't need to know everything about a car's mechanics to drive it.
**Example**
```java
abstract class A {
  abstract void display(); // Abstract method
}

class B extends A {
  void display() {
    System.out.println("Concrete method in Class B");
  }
}

public class Main {
  public static void main(String[] args) {
    A obj = new B(); // Abstraction
    obj.display(); // Concrete method call
  }
}


```
**Why Choose These Features:**
These features are the pillars of OOP. They allow for creating flexible, reusable, and maintainable code. They're essential for complex software development and make it easier to handle large applications.

[back to the top](#oop-interview-questions)

---

## 6. How do Interfaces Differ from Abstract Classes in OOP?

**Interviewer**: What's the difference between an interface and an abstract class in OOP?

**Interviewee**: In OOP, an interface is a contract that defines a set of methods without implementation, while an abstract class is a partially completed class that includes both abstract methods (without implementation) and concrete methods (with implementation). Interfaces represent capabilities, like a to-do list for classes. Abstract classes, on the other hand, provide a common foundation for subclasses.

**When to Use:**

**Interfaces:** Use interfaces when you want to define a contract for classes, especially when they are not related through inheritance. They are ideal for defining capabilities that can be added to any class, regardless of where that class is in the inheritance tree.
Abstract Classes: Use abstract classes when classes share a common structure and behavior, and you want to provide a base class that isn't supposed to be instantiated on its own.
Real-Life Example:

**Interface:** An interface is like a list of features a phone must have, like calling or messaging, regardless of the phone's brand or model.
Abstract Class: An abstract class is like a generic phone model that includes basic functionalities shared by all phones but isn't a complete phone by itself.
Performance Consideration:

While there's no significant performance difference between using interfaces and abstract classes, the choice significantly impacts design flexibility and future code maintenance.
*Why Choose One Over the Other:*

**Interfaces:** Choose interfaces when you need to enforce certain behaviors across a range of classes, especially when those classes don't share a common ancestor.
**Abstract Classes:** Choose abstract classes when you need to share code among closely related classes, with shared state or methods.


**Example**
```java
interface Drivable {
  void drive(); // Abstract method in interface
}

abstract class Vehicle {
  abstract void clean(); // Abstract method in abstract class
  void fillFuel() {
    System.out.println("Filling fuel"); // Concrete method
  }
}

class Car extends Vehicle implements Drivable {
  public void drive() {
    System.out.println("Car is driving"); // Implementing interface method
  }

  public void clean() {
    System.out.println("Car is clean"); // Implementing abstract class method
  }
}

public class Main {
  public static void main(String[] args) {
    Car myCar = new Car();
    myCar.drive(); // Interface method
    myCar.clean(); // Abstract class method
    myCar.fillFuel(); // Concrete method from abstract class
  }
}


```

[back to the top](#oop-interview-questions)

---

## 7. Does Java Support Multiple Inheritance?

**Interviewer:** Is multiple inheritance supported in Java?

**Interviewee:** Java does not support multiple inheritance with classes due to the "Diamond Problem," where a class can inherit from multiple classes and create ambiguity. However, Java supports multiple inheritance through interfaces, allowing a class to implement multiple interfaces.

**Interviewer:** But when you Have class C inherit from B and B inherit from A, C now have multiple inheritance because it's inherit multi class 

Here the interviewer will trick you, like what happened to me three years ago

**Interviewee:** C inherited B by direct inheritance and A by indirect inheritance 🖕


[back to the top](#oop-interview-questions)
