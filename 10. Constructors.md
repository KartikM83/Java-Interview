### 1. What is the constructor?

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
### 2. What happens if you don’t provide a constructor in a class?
if you don’t provide a constructor in a class in java, the compiler automatically generates the default constructor with no arguments.

---

### 3. How many types of constructors are used in Java?
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
### 4. What is the purpose of a default constructor?
The default constructor is useful for creating objects with initial default values,

--- 

### 5. Where and how can you use a private constructor?
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

### 6. What are the differences between the constructors and methods?

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

### 7. Can the constructor be inherited?

No, we can’t inherit a constructor.

---
