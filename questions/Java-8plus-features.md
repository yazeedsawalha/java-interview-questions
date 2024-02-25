
# Java +8 Features 

+ [Functional Interfaces](#functional-interfaces)
  + [Consumer](#consumer)
  + [Function](#function)
  + [Supplier](#supplier)
  + [Predicate](#predicate)
+ [Stream API](#stream-api)
+ [Lambda Expressions](#lambda-expressions)
+ [Method References](#method-references)
+ [Optional](#optional)
+ [CompletableFuture](#completablefuture)

## Functional Interfaces
Functional interfaces in Java are those that contain only one abstract method and can contain multiple default or static methods. They are designed to be used primarily with lambda expressions.

### Consumer
The `Consumer<T>` interface represents an operation that accepts a single input argument and returns no result. It's often used for iterating over collections.

#### Example:
```java
Consumer<String> printConsumer = System.out::println;
printConsumer.accept("Hello, Consumer!"); // Prints "Hello, Consumer!"
```

### Function
The `Function<T, R>` interface represents a function that accepts one argument and produces a result. This functional interface is used to apply transformations on data.

#### Example:
```java
Function<Integer, String> convert = x -> "Number: " + x;
System.out.println(convert.apply(5)); // Prints "Number: 5"
```

### Supplier
The `Supplier<T>` interface does not take any arguments but returns a value of type T. It can be used to generate or supply values without taking any input.

#### Example:
```java
Supplier<Double> randomValue = Math::random;
System.out.println(randomValue.get()); // Prints a random value
```

### Predicate
The `Predicate<T>` interface represents a predicate (boolean-valued function) of one argument. It is used to test objects to determine if they satisfy some criteria.

#### Example:
```java
Predicate<Integer> isPositive = x -> x > 0;
System.out.println(isPositive.test(5)); // true
System.out.println(isPositive.test(-5)); // false
```

## Stream API
The Stream API supports functional-style operations on streams of elements, such as map-reduce transformations.

### Example:
```java
List<String> names = Arrays.asList("John", "Doe", "Jane", "Doe");
names.stream()
    .filter(name -> name.startsWith("J"))
    .map(String::toUpperCase)
    .sorted()
    .forEach(System.out::println);
// Prints:
// JANE
// JOHN
```

## Lambda Expressions
Lambda expressions enable you to treat functionality as a method argument, or express instances of single-method interfaces (functional interfaces) more succinctly.

### Example:
```java
Runnable thread = () -> System.out.println("Running in a thread");
new Thread(thread).start(); // Running in a thread
```

## Method References
Method references are a shorthand notation of lambda expressions to call methods.

### Example:
```java
List<String> names = Arrays.asList("John", "Doe", "Jane", "Doe");
names.forEach(System.out::println);
```

## Optional
`Optional<T>` is a container object which may or may not contain a non-null value. It is used to avoid `NullPointerException`.

### Example:
```java
Optional<String> optionalName = Optional.ofNullable("John");
optionalName.ifPresent(name -> System.out.println("Name is " + name)); // Prints "Name is John"
```

## CompletableFuture
`CompletableFuture<T>` is used for asynchronous programming. It represents a future result of an asynchronous computation.

### Example:
```java
CompletableFuture.supplyAsync(() -> "Hello")
    .thenApply(result -> result + " World")
    .thenAccept(System.out::println); // Prints "Hello World"
```

This overview provides a deeper understanding of Java 8's key features, emphasizing functional programming and cleaner, more concise code.
