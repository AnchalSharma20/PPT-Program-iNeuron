Core Module assignment
======================
Assignment-1
------------
💡
Q1. What is the difference between Compiler and Interpreter
```
The main difference between a compiler and an interpreter is that a compiler translates the entire source
code into machine code before execution, while an interpreter translates and executes the source code line by line.
```

Q2. What is the difference between JDK, JRE, and JVM?
```
JDK stands for Java Development Kit, which includes tools for developing and compiling Java programs.
JRE stands for Java Runtime Environment, which provides the necessary runtime environment to run Java applications.
JVM stands for Java Virtual Machine, which is responsible for executing Java bytecode.
```

Q3. How many types of memory areas are allocated by JVM?
```
The JVM allocates different types of memory areas, including the heap, method area, stack, PC registers, and native method stack.
```

Q4. What is JIT compiler?
```
JIT (Just-In-Time) compiler is a component of the JVM that dynamically compiles parts of the bytecode into native machine code at runtime.
It aims to improve performance by identifying frequently executed code and optimizing it for faster execution.
```

Q5. What are the various access specifiers in Java?
```
In Java, the access specifiers determine the accessibility of classes, methods, and variables. 
The access specifiers are public, protected, default (no explicit specifier), and private.
```

Q6. What is a compiler in Java?
```
In Java, a compiler is a software tool that translates Java source code into bytecode, 
which is a platform-independent representation of the program. It performs syntax and semantic checks,
generates intermediate code, and prepares the program for execution on the JVM.
```

Q7. Explain the types of variables in Java?
```
In Java, there are three types of variables: instance variables (belonging to an instance of a class), 
static variables (associated with a class itself), and local variables (defined within a method or block).
```

Q8. What are the Datatypes in Java?
```
Java provides various data types, including primitive data types (such as int, boolean, float) 
and reference types (such as classes, interfaces, and arrays).
```

Q9. What are the identifiers in java?
```
Identifiers in Java are used to name classes, methods, variables, and other program elements.
They must follow certain rules, such as starting with a letter or underscore, consisting of letters, digits, or underscores, and not being a reserved keyword.
```

Q10. Explain the architecture of JVM
```
The architecture of the JVM consists of three main components: class loader, runtime data area, and execution engine.
The class loader loads class files, the runtime data area stores data during program execution, 
and the execution engine interprets or compiles bytecode into machine code for execution.
```

Assignment-2
-------------
Q1. What are the Conditional Operators in Java?
```
The conditional operators in Java are:
== (equal to)
!= (not equal to)
> (greater than)
< (less than)
>= (greater than or equal to)
<= (less than or equal to)
```

Q2. What are the types of operators based on the number of operands?
```
Operators in Java can be classified into three types based on the number of operands:
Unary operators (e.g., !, -)
Binary operators (e.g., +, -, *, /, %)
Ternary operator (only one: ?:, the conditional operator)
```

Q3. What is the use of Switch case in Java programming?
```
The switch statement in Java is used for multi-way branching. It allows the program to execute different code blocks 
based on the value of an expression or variable.
```

Q4. What are the conditional Statements and use of conditional statements in Java?
```
Conditional statements in Java are used to control the flow of execution based on certain conditions. 
The commonly used conditional statements are if, else if, and else. They help in executing specific blocks of code based on the evaluation of conditions.
```

Q5. What is the syntax of if else statement?
```Java
if (condition) {
    // code to be executed if the condition is true
} else {
    // code to be executed if the condition is false
}
```

Q6. How do you compare two strings in Java?
```Java
String str1 = "Hello";
String str2 = "World";

if (str1.equals(str2)) {
    // Strings are equal
} else {
    // Strings are not equal
}
```

Q7. What is Mutable String in Java Explain with an example
```
In Java, strings are immutable, meaning their values cannot be changed. However, using the StringBuilder class, you can create mutable strings.
```

Q8. Write a program to sort a String Alphabetically
```Java
import java.util.Arrays;

public class StringSortExample {
    public static void main(String[] args) {
        String input = "openai";
        char[] chars = input.toCharArray();
        Arrays.sort(chars);
        String sortedString = new String(chars);
        System.out.println(sortedString);
    }
}
```

Q9. Write a program to check if the letter 'e' is present in the word 'Umbrella'.
```Java
public class LetterCheckExample {
    public static void main(String[] args) {
        String word = "Umbrella";
        boolean containsE = word.contains("e");
        if (containsE) {
            System.out.println("The word contains the letter 'e'.");
        } else {
            System.out.println("The word does not contain the letter 'e'.");
        }
    }
}
```

Q10. Where exactly is the string constant pool located in the memory?
```
The string constant pool is located in the Java heap memory. It is a special area where string literals and interned strings are stored. 
The string pool allows efficient memory management by reusing string objects with the same value.
```

Assignment-3
------------
Q1. Write a simple Banking System program by using OOPs concept where you can get account Holder name balance etc?
```Java
class BankAccount {
    private String accountHolderName;
    private double balance;

    public BankAccount(String accountHolderName, double balance) {
        this.accountHolderName = accountHolderName;
        this.balance = balance;
    }

    public String getAccountHolderName() {
        return accountHolderName;
    }

    public double getBalance() {
        return balance;
    }
}

public class BankingSystem {
    public static void main(String[] args) {
        BankAccount account = new BankAccount("John Doe", 1000.0);
        System.out.println("Account Holder Name: " + account.getAccountHolderName());
        System.out.println("Balance: " + account.getBalance());
    }
}
```

Q2. Write a Program where you inherit method from parent class and show method Overridden Concept?
```Java
class Parent {
    public void display() {
        System.out.println("Parent class method");
    }
}

class Child extends Parent {
    @Override
    public void display() {
        System.out.println("Child class method");
    }
}

public class MethodOverridingExample {
    public static void main(String[] args) {
        Parent parentObj = new Parent();
        parentObj.display();  // Output: Parent class method

        Child childObj = new Child();
        childObj.display();  // Output: Child class method
    }
}
```

Q3. Write a program to show run time polymorphism in java?
```Java
class Animal {
    public void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    @Override
    public void sound() {
        System.out.println("Cat meows");
    }
}

public class RuntimePolymorphismExample {
    public static void main(String[] args) {
        Animal animal;

        animal = new Dog();
        animal.sound();  // Output: Dog barks

        animal = new Cat();
        animal.sound();  // Output: Cat meows
    }
}
```

Q4. Write a program to show Compile time polymorphism in java?
```Java
public class CompileTimePolymorphismExample {
    public static void add(int a, int b) {
        int sum = a + b;
        System.out.println("Sum of two integers: " + sum);
    }

    public static void add(double a, double b) {
        double sum = a + b;
        System.out.println("Sum of two doubles: " + sum);
    }

    public static void main(String[] args) {
        add(5, 10);        // Output: Sum of two integers: 15
        add(2.5, 3.5);     // Output: Sum of two doubles: 6.0
    }
}
```

Q5. Achieve loose coupling in java by using OOPs  concept?
```
Achieving loose coupling in Java can be done by using object-oriented programming concepts such as encapsulation, inheritance, and
interfaces. By creating classes with clear responsibilities and defining interfaces to communicate between them, you can reduce
dependencies and achieve loose coupling.
```

Q6. What is the benefit of encapsulation in java?
```
The benefit of encapsulation in Java is that it provides data hiding and protects the internal state of an object from being accessed
directly by other parts of the program. It allows for better control over data access and modification, enhances code maintainability,
and facilitates code reusability.
```

Q7. Is java a t 100% Object oriented Programming language? If no why ?
```
No, Java is not considered a 100% object-oriented programming language because it supports primitive data types, which are not objects.
Additionally, Java has features like static methods, static variables, and the concept of null, which are not strictly
object-oriented. However, Java is predominantly object-oriented and follows many object-oriented principles.
```

Q8. What are the advantages of abstraction in java?
```
The advantages of abstraction in Java are:
- It allows you to focus on the essential features of an object and hide unnecessary details.
- It helps in creating reusable code components through class inheritance and interfaces.
- It provides a clear separation between interface and implementation, allowing for easier maintenance and modification of code.
- It enhances code readability and understandability by providing a higher-level view of the system.
```

Q9. What is an abstraction explained with an Example?
```
Abstraction in Java refers to the process of creating abstract classes and interfaces to define common characteristics 
and behaviors that can be shared by multiple classes. It allows you to define methods without providing their implementation,
leaving it to the subclasses to implement those methods. Here's an example:
```
```Java
abstract class Shape {
    public abstract void draw();
}

class Circle extends Shape {
    @Override
    public void draw() {
        System.out.println("Drawing a circle");
    }
}

class Rectangle extends Shape {
    @Override
    public void draw() {
        System.out.println("Drawing a rectangle");
    }
}

public class AbstractionExample {
    public static void main(String[] args) {
        Shape circle = new Circle();
        circle.draw();      // Output: Drawing a circle

        Shape rectangle = new Rectangle();
        rectangle.draw();   // Output: Drawing a rectangle
    }
}
```

Q10. What is the final class in Java?
```
In Java, a final class is a class that cannot be subclassed. It is the opposite of an extendable or inheritable class.
When a class is marked as final, it means it cannot be extended by other classes to inherit its properties or behaviors.
Additionally, all methods in a final class are implicitly final as well, meaning they cannot be overridden by subclasses.
Final classes are often used for utility classes or classes that provide constants or helper methods.
```

Assignment-4
------------
Q1. Write a program to show Interface Example in java?
```Java
interface Shape {
    void draw();
}

class Circle implements Shape {
    @Override
    public void draw() {
        System.out.println("Drawing a circle");
    }
}

class Rectangle implements Shape {
    @Override
    public void draw() {
        System.out.println("Drawing a rectangle");
    }
}

public class InterfaceExample {
    public static void main(String[] args) {
        Shape circle = new Circle();
        circle.draw();      // Output: Drawing a circle

        Shape rectangle = new Rectangle();
        rectangle.draw();   // Output: Drawing a rectangle
    }
}
```

Q2. Write a program a Program with 2 concrete method and 2 abstract method in java ?
```Java
abstract class Parent {
    public void concreteMethod1() {
        System.out.println("Concrete Method 1");
    }

    public void concreteMethod2() {
        System.out.println("Concrete Method 2");
    }

    public abstract void abstractMethod1();

    public abstract void abstractMethod2();
}

class Child extends Parent {
    @Override
    public void abstractMethod1() {
        System.out.println("Abstract Method 1 implementation in Child class");
    }

    @Override
    public void abstractMethod2() {
        System.out.println("Abstract Method 2 implementation in Child class");
    }
}

public class AbstractMethodExample {
    public static void main(String[] args) {
        Child child = new Child();
        child.concreteMethod1();     // Output: Concrete Method 1
        child.concreteMethod2();     // Output: Concrete Method 2
        child.abstractMethod1();     // Output: Abstract Method 1 implementation in Child class
        child.abstractMethod2();     // Output: Abstract Method 2 implementation in Child class
    }
}
```

Q3. Write a program  to show the use of functional interface in java?
```Java
@FunctionalInterface
interface MathOperation {
    int operate(int a, int b);
}

public class FunctionalInterfaceExample {
    public static void main(String[] args) {
        MathOperation addition = (a, b) -> a + b;
        int result = addition.operate(5, 3);
        System.out.println("Result: " + result);    // Output: 8
    }
}
```

Q4. What is an interface in Java?
```
An interface in Java is a reference type that defines a contract of methods that a class implementing the interface must follow.
It acts as a blueprint for classes to provide the implementation of the methods defined in the interface.
Interfaces can contain constant fields and default methods in addition to abstract methods.
```

Q5. What is the use of interface in Java?
```
The use of interfaces in Java is to achieve abstraction and provide a way to achieve multiple inheritance of type. 
It allows classes to implement multiple interfaces, enabling them to inherit the behaviors defined by those interfaces. 
Interfaces are also used to establish a contract between different parts of a program.
```

Q6. What is the lambda expression of Java 8?
```
Lambda expressions in Java 8 are a concise way to represent anonymous functions. 
They allow you to write more compact code by expressing behavior as a method argument or code block.
Lambda expressions are typically used in functional interfaces, which are interfaces with a single abstract method.
```

Q7. Can you pass lambda expressions to a method? When?
```
Yes, lambda expressions can be passed as arguments to methods. This is possible when the method parameter is of a functional interface type,
meaning the interface has a single abstract method. The lambda expression provides an implementation for that method.
```

Q8. What is the functional interface in Java 8?
```
A functional interface in Java 8 is an interface that has only one abstract method.
It is also known as a Single Abstract Method (SAM) type or a functional interface.
Functional interfaces are used to leverage lambda expressions and method references in Java 8's functional programming features.
```

Q9. What is the benefit of lambda expressions in Java 8?
```
The benefits of lambda expressions in Java 8 include:
- Concise syntax: Lambda expressions allow you to write compact and expressive code, reducing boilerplate code.
- Readability: They improve code readability by focusing on the behavior rather than the mechanics of implementation.
- Functional programming: Lambda expressions facilitate functional programming paradigms, enabling you to write code in a more declarative and expressive style.
- Code reuse: Lambda expressions promote code reuse and enable the passing of behavior as data.
- Parallelism and concurrency: They support parallel programming by easily enabling the use of multi-threading and asynchronous programming.
```

Q10. Is it mandatory for a lambda expression to have parameters?
```
No, it is not mandatory for a lambda expression to have parameters.
Lambda expressions can have zero or more parameters depending on the functional interface they are associated with.
For example, a lambda expression with no parameters would have an empty parameter list: () -> { /* code */ }.
```

Assignment-5
------------
Q1. What is Exception in Java?
```
In Java, an exception is an event that occurs during the execution of a program, disrupting the normal flow of the program.
It represents an abnormal condition or an error situation. Exceptions can occur due to various reasons, such as invalid input,
resource unavailability, or programming errors.
```

Q2. What is Exception Handling?
```
Exception handling is the process of dealing with exceptions that occur during the execution of a program.
It involves catching and handling exceptions to prevent abrupt termination of the program. Exception handling
allows the program to gracefully recover from errors and take appropriate actions.
```

Q3. What is the difference between Checked and Unchecked Exceptions and Error?
```
Checked exceptions are checked at compile-time, and the programmer is required to handle them using try-catch blocks 
or declare them in the method signature using the throws keyword. Unchecked exceptions are not checked at compile-time and 
can occur during runtime. Errors, on the other hand, are severe issues that typically cannot be recovered from, such as
OutOfMemoryError or StackOverflowError.
```

Q4. What are the difference between throw and throws in Java?
```
In Java, throw is used to explicitly throw an exception within a method or block of code.
It is followed by an instance of an exception class or a subclass of Throwable. On the other hand, 
throws is used in the method declaration to indicate that the method may throw one or more exceptions.
It specifies the types of exceptions that the method might throw to the caller.
```

Q5. What is multithreading in Java? mention its advantages
```
Multithreading in Java refers to the concurrent execution of multiple threads within a single program.
It allows multiple tasks to be executed simultaneously, improving the efficiency and responsiveness of the program. 
Some advantages of multithreading in Java include:
- Increased performance by utilizing multiple CPU cores.
- Enhanced responsiveness and user experience in GUI applications.
- Efficient handling of I/O operations, such as reading from or writing to files or network connections.
- Simplified coding for concurrent or parallel processing tasks.
```

Q6. Write a program to create and call a custom exception
```Java
class CustomException extends Exception {
    public CustomException(String message) {
        super(message);
    }
}

public class CustomExceptionExample {
    public static void main(String[] args) {
        try {
            throw new CustomException("This is a custom exception");
        } catch (CustomException e) {
            System.out.println(e.getMessage());
        }
    }
}
```

Q7. How can you handle exceptions in Java? 
```
Exceptions in Java can be handled using try-catch blocks. The code that might throw an exception is enclosed within the try block, 
and the potential exceptions are caught and handled in the catch block. Additionally, the finally block can be used to execute code
that should always be executed, regardless of whether an exception occurs or not.
```

Q8. What is Thread in Java?
```
In Java, a thread is a lightweight unit of execution within a program. It represents an independent path of execution, 
allowing multiple threads to run concurrently. Threads are used to achieve multithreading and perform concurrent tasks in a program.
```

Q9. What are the two ways of implementing thread in Java?
```
There are two ways of implementing threads in Java:

1. By extending the Thread class: You can create a subclass of the Thread class and override its run() method to define the task to be executed by the thread.
2. By implementing the Runnable interface: You can implement the Runnable interface and provide the task's implementation in the run() method.
Then, create an instance of the class and pass it to a Thread object.
```

Q10. What do you mean by garbage collection?
```
Garbage collection in Java is the automatic process of reclaiming memory occupied by objects that are no longer referenced and are considered
eligible for destruction. The Java Virtual Machine (JVM) automatically manages the allocation and deallocation of memory for objects.
When an object is no longer reachable, the garbage collector identifies and releases the memory occupied by that object,
making it available for future allocations. Garbage collection helps in memory management, preventing memory leaks and manual memory deallocation.
```

Assignment-6
------------
Q1. What is Collection in Java? 

```
In Java, a Collection is a framework that provides an architecture to store and manipulate a group of objects.
It provides interfaces, implementations, and algorithms to work with collections of elements.
```

Q2. Differentiate between Collection and collections in the context of Java.

```
In Java, "Collection" refers to the Collection framework, which is a set of interfaces and classes that provide high-level
functionality to work with groups of objects. "collections" (with a lowercase 'c') generally refers to the various
concrete implementations of the Collection interfaces, such as ArrayList, LinkedList, HashSet, etc.
```

Q3. What are the advantages of the Collection framework?

```
The advantages of the Collection framework in Java include:
1. Provides a standard way to store and manipulate groups of objects.
2. Offers reusable and well-tested implementations of common data structures and algorithms.
3. Facilitates code reusability, as different components can interact using the standard Collection interfaces.
4. Simplifies the development process by providing high-level operations for searching, sorting, and modifying collections.
5. Supports polymorphism, allowing different implementations of collections to be used interchangeably.
```

Q4. Explain the various interfaces used in the Collection framework.

```
The Collection framework in Java includes several interfaces, such as:
Collection: The root interface that defines basic operations common to all collections, such as adding, removing, and querying elements.
List: An ordered collection that allows duplicate elements and provides positional access to elements.
Set: A collection that does not allow duplicate elements and provides no specific order for its elements.
Queue: A collection designed for holding elements before processing, often following the FIFO (First-In-First-Out) order.
Map: An object that maps keys to values, where each key is unique and associated with a value.
```

Q5. Differentiate between List and Set in Java.

```
The main differences between List and Set in Java are:
1. List allows duplicate elements, while Set does not allow duplicates.
2. List maintains the insertion order of elements, whereas Set does not guarantee any specific order.
3. List provides positional access to elements using indices, while Set does not provide positional access.
4. List implementations (e.g., ArrayList, LinkedList) allow multiple elements with the same value, while Set implementations (e.g., HashSet, TreeSet) enforce uniqueness.
```

Q6. What is the Differentiate between Iterator and ListIterator in Java.

```
The main differences between Iterator and ListIterator in Java are:
- Iterator is a universal interface that can be used with various collection types, while ListIterator is specific to List implementations.
- Iterator allows forward-only traversal of elements, while ListIterator allows bidirectional traversal (both forward and backward).
- ListIterator provides additional operations such as adding, replacing, and retrieving elements at any position in the List.
- ListIterator has methods like previous() and hasPrevious() that are not present in the Iterator interface.
```

Q7. What is the Differentiate between Comparable and Comparator

```
The main differences between Comparable and Comparator in Java are:
- Comparable is an interface that defines a natural ordering for objects of a class. The class itself must implement the Comparable interface to specify its own ordering.
- Comparator is an interface that allows for the comparison of objects based on a custom logic defined by a separate class.
- The Comparable interface's compareTo() method is used for object comparison, while the Comparator interface's compare() method is used for custom comparison logic.
- The Comparable interface is typically used for comparing objects within the same class, while Comparator is used for comparing objects from different classes or when multiple comparison logics are needed.
```

Q8. What is collision in HashMap?

```
In HashMap, collision occurs when two or more keys map to the same hash code and are then stored in the same bucket. To handle collisions, HashMap uses a technique called "chaining." Each bucket in the HashMap contains a linked list of entries. When a collision occurs, new entries are added to the linked list in the bucket, forming a chain.
```

Q9. Distinguish between a hashmap and a Treemap.

```
The main differences between HashMap and TreeMap in Java are:
- HashMap is an unordered collection based on hash table implementation, while TreeMap is a sorted collection based on a red-black tree implementation.
- HashMap provides faster access and retrieval of elements using keys, as it uses hashing for efficient lookup. TreeMap provides ordered traversal and retrieval of elements based on the natural ordering of keys or a custom comparator.
- HashMap allows null keys and values, while TreeMap does not allow null keys but allows null values (only if the comparator allows it).
- HashMap has average constant-time performance for insertion, deletion, and retrieval operations. TreeMap has O(log n) time complexity for these operations.
```

Q10. Define LinkedHashMap in Java
```
- LinkedHashMap is a subclass of HashMap that maintains the insertion order of entries. It is implemented as a hash table with a doubly-linked list running through all of its entries.
- The linked list allows predictable iteration order based on the order of insertion.
- LinkedHashMap provides the same performance characteristics as HashMap, with additional overhead for maintaining the linked list.
```
