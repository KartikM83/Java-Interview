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

	
