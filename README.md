# Java-Interview

### 1. Is Java Platform Independent if then how?
Yes, Java is a Platform Independent language javac compiles the program to form a bytecode this bytecode is a platform independent so to run these bytecode we need jvm preinstalled in the operating system Although ****JVM is platform dependent****,
so the bytecode can be created on any system that makes java platform independent

---
**2. What is JVM?**
the JVM stand for java virtual machine it is responsible for loading,  verifying and executing the bytecode

---

**3. What is JIT ?**
- JIT is a Just in time compilation.  This technique is used by the JVM to improve the performance  of the java program

- it is resposible for converting the bytecode into native machine code at runtime before the code is executed

---
### 4 . What are Memory storages available with JVM?
1) **Class Area:** Stores class-level data, such as class definitions, static variables, method definitions, and metadata related to loaded classes.

2) **Heap:** Stores objects and their associated instance variables at runtime.
3) **Stack:** Stores local variables and function/method call data (activation records).
4) **Program Counter Register:** stores the address of the Java virtual machine instruction currently being executed.

5) **Native method Stack:** stores all the native methods used in the application.

---

### 5. What is a classloader?
Classloader is the part of Java Runtime Environment during the execution of the bytecode the  classloader is responsible for dynamically loading the java classes and interfaces to JVM  Because of classloaders Java run time system does not need to know about files and file systems.

---

### 6. What Is JRE ? 
JRE stands for Java Runtime Environment, it is an installation package that provides an environment to run the Java program on any machine.

---

### 7. What is JDK? 
JDK stands for Java Development Kit which provides the environment to develop and execute Java programs. JDK is a package that includes two things Development Tools to provide an environment to develop your Java programs and, JRE to execute Java programs or applications.

----
### 8. What is Java String Pool?
A string pool is a place i  heap in which all the string defined in the program are stored and there is a separate place in stack in which the variable is store that pointing the string value .

---

### 9. What is the Wrapper class in Java?
Wrapper class in java is a class that provides a way to use primitive data types as a object. Java provides wrapper class for every primitive data types allowing them to treated as object in the situation where the object is needed such as Arraylist.


### 10. Why do we need wrapper classes?

1.  **Wrapper classes** are essential for using **primitives** as **objects** in contexts like **collections**.
2. Wrapper classes are final and immutable
3.  Provides methods like valueOf(), parseInt(), etc.
4.  It provides the feature of autoboxing and unboxing.

---

### 11.  What is autoboxing and unboxing ?
**Autoboxing**: The automatic conversion of primitive types to their corresponding wrapper class objects. 
Example
```java
int num = 10;
Integer obj = num; // Autoboxing

```

**Unboxing**: The automatic conversion of wrapper class objects to their corresponding primitive types. 
Example:
```java 
Integer obj = 10;
int num = obj; // Unboxing
```

---

### 12. Differentiate between instance and local variables.
**Insatnce Variable**
1.  It is declared outside the method, constructor or block and directly invoked by the method.
2. It has default value.
3. It can be used throughout the class.
4. Lifespan as long as the  object is exists

**Local Variable:** 
5. It is declared within the method or block .
6. No default value
7. the scope is limited to the method.
8. Lifespan  As long as the method/block is executing

---
### 13.  Explain the difference between instance variable and a class variable.

**Insatnce Variable**
1. Instance variable is a variable that are associated with the instance of the class. Every object of the class has it own copy of the instance variable
2. Instance variable are declared without the static keyword inside a class but outside any method or block.
3. Lifespan  Lifespan as long as the  object is exists
4. Stored in **heap memory** (one copy per object)

**Class Variable ( Static variable )**
5.  A class variable is a variable that is shared by all instances (objects) of a class. There is only one copy of the variable within the class.
6.  Static variable are declared the static keyword inside a class but outside any method or block.
7. Lifespan  Lifespan as long as the  class is exists
8. Stored in **method area** (one copy for the class)

---

### 14. What is the difference between System.out, System.err, and System.in?
**System.out**
- It us used to print the output to the terminal
- It is a instance of printStream so we can use method like println(), print(), printf()

**System.err**

-It used to display the error message.
-It is a instance of printStream so we can use method like println(), print(), printf()

**System.in**
-It is used to take inputs from the user 
- It is an instance of `InputStream`, which allows you to read bytes from the standard input.
- We can’t use the System.in directly so we use Scanner class for taking input with the system.in.

---

### 15. Difference in the use of print, println, and printf.

**1. Print**:  Used to output text without moving to a new line.
**2. Println**: Prints the text followed by a new line.
**3. Printf**: Used for formatted output.

---

### 16. What is the difference between the Reader/Writer class hierarchy and the InputStream/OutputStream class hierarchy?

- The key difference between them is that byte stream data is read and written by input/output stream classes.
- Characters are handled by the Reader and Writer classes. 
- Reader/Writer classes\ accept character arrays as parameters, 
- input/output stream class methods accept byte arrays. 
- In comparison to input/output streams, the Reader/Writer classes are more efficient, handle all Unicode characters.


---
### 17. What are the super most classes for all the streams?

All the stream classes can be divided into two types of classes that are ByteStream classes and CharacterStream Classes. The ByteStream classes are further divided into InputStream classes and OutputStream classes. CharacterStream classes are also divided into Reader classes and Writer classes. The SuperMost classes for all the InputStream classes is java.io.InputStream and for all the output stream classes is java.io.OutPutStream. Similarly, for all the reader classes, the super-most class is java.io.Reader, and for all the writer classes, it is java.io.Writer.


---

### 18. What are operators?

Operators are the special types of symbols used for performing some operations over variables and values


---
### 19. Explain the difference between >> and >>> operators.

**>>**: Shifts the bits of a number to right by specified number of position and it preserve the sign of the number 
- For **Positive number** the leftmost bits filled with zero
- For **Negative number** the leftmost bits filled with  1
- This is called an **Arithmetic Shift**.

**Example**
```java
int a = 8;     // In binary: 1000
int b = a >> 2; // Shift right by 2 positions
System.out.println(b); // Output: 2 (binary 0010)
```

```java
int c = -8;    // In binary (32-bit): 11111111111111111111111111111000
int d = c >> 2; // Shift right by 2 positions
System.out.println(d); // Output: -2 (binary 11111111111111111111111111111110)
```

**>>>**: Shifts the bits of number to right with the specified number of position but it treat number unsigned

 - It filled leftmost bits with 0 even the number eighter **Positive** or **Negative**
 - This is called a **Logical Shift**.
 
 **Example**
```java
int a = 8;     // In binary: 1000
int b = a >>> 2; // Shift right by 2 positions
System.out.println(b); // Output: 2 (binary 0010)
```
```java
int c = -8;    // In binary (32-bit): 11111111111111111111111111111000
int d = c >>> 2; // Shift right by 2 positions
System.out.println(d); // Output: 1073741822 (binary 00111111111111111111111111111110)
```

---
### 20. Which Java operator is right associative?
There is only one operator which is right associative which is = operator.

-   **Left-associative** (the default for most operators): Operators are evaluated from **left to right**.
-   **Right-associative**: Operators are evaluated from **right to left**.

---
### 21. What is dot operator?
The **dot operator (`.`)** is used to access members (like fields, methods, or properties) of an object or class

---

### 22. What is covariant return type?
It is a concept in object oriented programing where the method in subclass overrides the method in superclass and the return type of the override method is subtype of the return type of the superclass.

```java
class Animal {
    Animal makeSound() {
        return new Animal();
    }
}

class Dog extends Animal {
    @Override
    Dog makeSound() {  // Covariant return type
        return new Dog();
    }
}
```

---
### 23. What is the transient keyword?
The transient keyword is used at the time of serialization if you don't want to save the value of the variable  in file. JVM compile the code but ignores the original value and set the default value of the data type.

### 24. What are the differences between String and StringBuffer?

**String**: 

 - String Is a **immutable** means once you assign the value to the string it cannot change.(If you try to modify String create new string object)
 - Because of the immutability of the String, If you perform many operation on string it will create new String object every time this leads to more memory usage and slower the performance.
 - Since `String` objects are **immutable**, they are **thread-safe** by nature. Multiple threads can access a `String` without synchronization issues.
 - Use `String` when you don't need to modify the string value frequently.
 
**StringBuffer**: 
 - `StringBuffer` is mutable, you can modify the value of the StringBuffer object without creating new object it allow you to change its content.
 - Because of the mutability of the StringBuffer, If you perform many operation on StringBuffer it will modify the contents of the existing `StringBuffer`without creating new object making it more efficient  memory usage and faster
 - **Thread-safe** because it has **synchronized methods**.
 - Use `StringBuffer` when you need to perform multiple modifications or concatenations of strings

**StringBuilder**

-The **`StringBuilder`** class in Java is similar to **`StringBuffer`**, but with one key difference: **`StringBuilder` is not synchronized**. This means that `StringBuilder` is not thread-safe, but it provides better performance than `StringBuffer` in situations where thread safety is not a concern.

---

### 25. What is an array in Java?
An **array** in Java is a **collection** of **similar types of data elements** that are stored in a **fixed-size** structure.
- once you assign the size of array it cannot change.
- The array element  can be access through the index 
- The array indexing always starts with zero.
```java
int[] Arr = new int[5];
```

---
### 26. On which memory arrays are created in Java?
-   The **array reference** is stored in the **stack** memory.
-   The **array data** (its elements) is stored in the **heap** memory.

(Heap Memory is the part of memory where objects (including arrays) are stored in Java. When you create an array, it is treated as an object, and therefore, it is allocated memory in the heap.)

---

### 27. What are the types of an array?
- ****Single-Dimensional Arrays:**** Arrays that have only one dimension
-   ****Multi-Dimensional Arrays:**** Arrays that have two or more dimensions such as two-dimensional or three-dimensional arrays.

---
### 28. What is the difference between int array[] and int[] array?
Both int array[] and int[] array are used to declare an array of integers in java. The only difference between them is on their syntax no functionality difference is present between them.

---
### 29. How to copy an array in Java?
-   ****clone() method in Java:**** This method in Java is used to create a shallow copy of the given array which means that the new array will share the same memory as the original array.
```java
int[] Arr = { 1, 2, 3, 5, 0};  
int[] tempArr = Arr.clone();
```

-   ****arraycopy() method:**** To create a deep copy of the array we can use this method which creates a new array with the same values as the original array.
```java
int[] Arr = {1, 2, 7, 9, 8};  
int[] tempArr = new int[Arr.length];  
System.arraycopy(Arr, 0, tempArr, 0, Arr.length);
```
-   ****copyOf() method:**** This method is used to create a new array with a specific length and copies the contents of the original array to the new array.
```java
int[] Arr = {1, 2, 4, 8};  
int[] tempArr = Arrays.copyOf(Arr, Arr.length);
```

-   ****copyOfRange() method:**** This method is very similar to the copyOf() method in Java, but this method also allows us to specify the range of the elements to copy from the original array.
```java
int[] Arr = {1, 2, 4, 8};  
int[] temArr = Arrays.copyOfRange(Arr, 0, Arr.length);
```

---
### 30. What do you understand by the jagged array?
A jagged Array in Java is just a two-dimensional array in which each row of the array can have a different length. Since all the rows in a 2-d Array have the same length but a jagged array allows more flexibility in the size of each row.

```java
int[][] Arr = new int[][] {  
 {1, 2, 8},   
 {7, 5},   
 {6, 7, 2, 6}  
};
```

---
### 31. What are the advantages and disadvantages of an array?

| Advantages | Disadvantages |
|--|--|
| Fast access to elements (O(1) time complexity) | Fixed size (cannot resize after creation) |
|  Simple to use and implement| Memory wastage if array is too large for data|
| Efficient use of memory|Cannot store different data types |
|Cache-friendly and good for large data sets|Inserting/deleting elements is inefficient|
| Easy to use in algorithms | Limited built-in methods for common operations |

---

### 32. What is an object-oriented Programming? 
**Object-Oriented Programming (OOP)** is a programming paradigm that organizes software design around data, or objects, rather than functions and logic. The primary concept of OOP is to create **objects** that interact with each other to perform tasks.

---
### 33. What are the main concepts of OOPs in Java?

The main concepts of OOPs in Java are mentioned below:

-   Inheritance
-   Polymorphism
-   Abstraction
-   Encapsulation
---
### 34. What is the difference between an object-oriented programming language and an object-based programming language?

An **object-oriented programming language** is a programming language that fully supports the principles of **object-oriented programming**, including all four key OOP concepts: **encapsulation**, **inheritance**, **polymorphism**, and **abstraction**.

**Examples**: Java, C#, etc.


An **object-based programming language** is a programming language that **supports objects** and **encapsulation**, but **lacks full support for inheritance** and/or **polymorphism**. These languages allow you to define and use objects, but they don't have all the features of  object-oriented programming languages.

**Examples**: Java script, visual basics, etc.

---

### 35. How is the ‘new’ operator different from the ‘newInstance()’ operator in Java?

the new operator is used to create objects, but if we want to decide the type of object to be created at runtime, there is no way we can use the new operator. In this case, we have to use the newInstance() method

---

### **36. What are Classes in Java?**

A **class** in Java is a blueprint or template for creating objects. It defines the **state** (variables) and **behavior** (methods) that objects of the class will have.

---

### 37. What is the difference between static (class) method and instance method?



| Features | **Static Method** | **Instance Method** |
|----------|----------|----------|
| **Belongs To** | Static method is belong to the class not to specific object.  | Instance method Belongs to an object of the class.  |
| **Declared with** |  It Is Define Using Static Keyword. | Not define with the Static keyword |
| **Access to variables and Method** | Static methods can access only static variable and method of the class.  | Instance method can access both **static** and **instance** variables and method of class |
| **Invocation** | Static methods can be called using the class name only without creating an instance of a class. | The instance methods can be called on a specific instance of a class using the object reference.|
| **Access to `this`** | Static methods do not have access to ****this**** keyword | Instance methods have access to ****this**** keyword|
| **Overridden** |Static methods cannot be overridden because they are resolved at compile time, not at run time. | Instance methods can be overridden because they are resolved at run time, not at compile time|


----
### 38. What is this keyword in Java?
‘this’ is a keyword used to reference a variable that refers to the current object.

----
### 39. What are Access Specifiers and Types of Access Specifiers?

Access Specifiers in use to restrict the scope of a class, constructor, variable, method, or data member. There are four types of Access Specifiers in Java mentioned below:

1.  **Public -** The code is accessible for all classes
2.  **Private -** The code is only accessible within the declared class
3.  **Protected -** The code is accessible in the same package and **subclasses**. You will learn more about subclasses and superclasses.
4.  **Default -** The code is only accessible in the same package. This is used when you don't specify a modifier.

---
### 40. What will be the initial value of an object reference which is defined as an instance variable?

The initial value of an object reference which is defined as an instance variable is a NULL value.

---
### 41. What is an object?
Object is a instance of class and it an entity that as state and behavior.

---
### 42. What are the different ways to create objects in Java?
1.  Using new keyword
2.  Using new instance
3.  Using clone() method
```java
class Car implements Cloneable {
    String model;

    Car(String model) {
        this.model = model;
    }

    void display() {
        System.out.println("Car model: " + model);
    }

    @Override
    protected Object clone() throws CloneNotSupportedException {
        return super.clone();  // Using Object's clone method
    }
}

public class Main {
    public static void main(String[] args) throws CloneNotSupportedException {
        // Creating an object and then cloning it
        Car originalCar = new Car("Ford");
        Car clonedCar = (Car) originalCar.clone();
        
        clonedCar.display();  // Outputs: Car model: Ford
    }
}
```

4.  Using deserialization
5.  Using the newInstance() method of the Constructor class

---
### 43. What is the constructor?

Constructor is a special method that is used to initialize objects. Constructor is called when a object is created. The name of constructor is same as of the class.

```java
// Class Created  
class XYZ{  
 private int val;  
    
 // Constructor  
 public XYZ(){  
 val=0;  
 }  
};
```

---
### 44. What happens if you don’t provide a constructor in a class?
if you don’t provide a constructor in a class in java, the compiler automatically generates the default constructor with no arguments.

---

### 45. How many types of constructors are used in Java?
**1. Default Constructor:** 

 - Default Constructor is a constructor that does not accept any parameter .
 - It initializes the object with default values. (0,null)
```java class MyClass {
    int number;

    // Default constructor
    MyClass() {
        number = 0;  // Initialize with default value
    }
}
```

**2 Parameterized Constructor**

- A constructor that accepts one or more parameters.
- It allows the initialization of an object with specific values passed at the time of object creation.
```java
class MyClass {
    int number;

    // Parameterized constructor
    MyClass(int num) {
        number = num;  // Initialize with the provided value
    }
}
```
---
### 46. What is the purpose of a default constructor?
The default constructor is useful for creating objects with initial default values,

--- 

### 47. Where and how can you use a private constructor?
1. **Singleton Design Pattern**
-   **Purpose:** The most common use of a private constructor is in the **Singleton pattern**, which ensures that only **one instance** of a class is created throughout the application's lifecycle.
-   **How it works:** The constructor is private so that the class cannot be instantiated from outside the class. Instead, the instance is created internally within the class and accessed via a **public static method**.
```java
class Singleton {
    // The single instance of the class
    private static Singleton instance;
    
    // Private constructor prevents instantiation from outside the class
    private Singleton() {
        // Initialization code here
    }
    
    // Public method to provide access to the instance
    public static Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }
}

public class Main {
    public static void main(String[] args) {
        // Access the Singleton instance
        Singleton obj = Singleton.getInstance();
    }
}
```
**Explanation:** The `Singleton` class can only be instantiated via the `getInstance()` method, and the constructor is private to ensure only one instance is created.

---

### 48. What are the differences between the constructors and methods?

**constructors** 

 - A constructor is used to **initialize** an object when it is created.
 - constructor **must have the same name** as the class
 - A constructor **does not have a return type**
 - A constructor is **invoked automatically** when a new object of the class is created using the `new` keyword.
 - Not inherited, but can call parent constructor using `super()`

**Method**

 - methods can be called multiple times during the life of an object.
 - A method can have any name
 - A method **must have a return type**,
 - A method is **called explicitly** on an object after the object has been created.
 - Inherited and can be overridden

---
### 49. What is an Interface?
- A interface is a blueprint of class which has abstract method, static method with no body  and  constant. it is used to specify a **contract** or **set of capabilities** that a class can implement 
- It does not have constructor

**Some Point keep in mind**
---
**Abstract Methods**:
An interface typically contains abstract methods (methods without a body), which must be implemented by any class that implements the interface.

```java
interface Animal {
    void sound(); // abstract method
}

```
**Multiple Inheritance**:
Java allows a class to implement multiple interfaces, which is a way to achieve multiple inheritance (as Java doesn’t support multiple inheritance through classes).

```java
interface Animal {
    void sound();
}

interface Mammal {
    void walk();
}

class Dog implements Animal, Mammal {
    public void sound() {
        System.out.println("Bark");
    }
    public void walk() {
        System.out.println("Dog is walking");
    }
}
```
**Constants**:
All variables declared inside an interface are implicitly `public`, `static`, and `final` (constant). They must be initialized when declared.
```java
interface Animal {
    int MAX_AGE = 100; // This is implicitly public, static, and final
}
```
### Example
```java
// Define the interface (Blueprint)
interface Animal {
    // Abstract method (no implementation)
    void sound();  // Each animal must have a sound method
    
    void eat();    // Each animal must have an eat method
}

// Class Dog implementing the Animal interface
class Dog implements Animal {
    @Override
    public void sound() {
        System.out.println("Bark");
    }
    
    @Override
    public void eat() {
        System.out.println("Dog is eating");
    }
}

// Class Cat implementing the Animal interface
class Cat implements Animal {
    @Override
    public void sound() {
        System.out.println("Meow");
    }
    
    @Override
    public void eat() {
        System.out.println("Cat is eating");
    }
}

public class Main {
    public static void main(String[] args) {
        // Polymorphism: Animal reference can point to different object types
        Animal dog = new Dog();
        Animal cat = new Cat();
        
        dog.sound();  // Outputs: Bark
        dog.eat();    // Outputs: Dog is eating
        
        cat.sound();  // Outputs: Meow
        cat.eat();    // Outputs: Cat is eating
    }
}
```

----
### 50. Give some features of the Interface. why use java interface
- Used to achieve abstraction.
- By interface we can support the functionality if multiple inheritance
-   It is also used to achieve loose coupling.
---
### 51. What is a marker interface?

An Interface is recognized as an empty interface (no field or methods) it is called a marker interface. Examples of marker interfaces are Serializable, Cloneable, and Remote interfaces.

---
### 52. What are the differences between abstract class and interface?

| **Aspect**                                   | **Abstract Class**                             | **Interface Class**                           |
|----------------------------------------------|------------------------------------------------|-----------------------------------------------|
| **Methods**                                  | Both abstract and non-abstract methods may be found in an abstract class. | The interface contains only abstract methods. |
| **Final Methods**                            | Abstract class supports final methods.         | Interface class does not support final methods.|
| **Multiple Inheritance**                     | Multiple inheritance is **not** supported by the Abstract class. | Multiple inheritance is **supported** by Interface Class. |
| **Keyword**                                  | `abstract` keyword is used to declare an abstract class. | `interface` keyword is used to declare the interface class. |
| **Extending/Implementing**                   | `extend` keyword is used to extend an Abstract Class. | `implements` keyword is used to implement the interface. |
| **Members Visibility**                       | Abstract class can have members like `protected`, `private`, etc. | All class members are `public` by default in an interface. |


---
### 53. What do you mean by data encapsulation?
Encapsulation means wrapping a data and information under a single unit.

---
### 54. What are the advantages of Encapsulation in Java?
 **1. Data Hiding (Access Control)**
 Data hiding means hiding the internal data within the class to prevent it direct access form the outside the class
```java
class Person {
    private String name; // private field (encapsulated)
    
    // Getter method
    public String getName() {
        return name;
    }
    
    // Setter method
    public void setName(String name) {
        if(name != null && !name.isEmpty()) {
            this.name = name;
        }
    }
}


```
Here, the `name` field is **private**, and it cannot be directly accessed from outside the `Person` class. Instead, we control access via the **getter** and **setter** methods.

**2. Improved Maintainability**:

When you encapsulate data within a class, any changes to the internal workings (implementation details) of the class do not affect other parts of the program. As long as the public interface remains the same (the getters and setters), you can modify the internal implementation without worrying about breaking other code that uses the class.

**3. Increased Flexibility and Reusability**:

Encapsulation makes it easier to change or extend the functionality of a class. Since the implementation is hidden from the outside, you can modify it without disrupting other parts of the application. Additionally, classes that use encapsulation are more reusable because the internal behavior is abstracted away.

**4. Control Over Data**:

hrough encapsulation, you can control how data is accessed and modified. For example, you can include validation logic in setters to ensure that only valid data is assigned to a variable. This ensures that the object is always in a valid state.

---

	
