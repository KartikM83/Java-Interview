# Java-Interview

Is Java Platform Independent if then how?
Yes, Java is a Platform Independent language javac compiles the program to form a bytecode this bytecode is a platform independent so to run these bytecode we need jvm preinstalled in the operating system Although JVM is platform dependent,
so the bytecode can be created on any system that makes java platform independent
What is JVM?
the jvm stand for java virtual machine it is resposible for loading, verifiying and executing the bytecode

What is JIT ?
JIT is a Just in time compilation. This techinique is used by the JVM to improve the performance of the java program

it is resposible for converting the bytecode into native machine code at runtime before the code is executed

5. What are Memory storages available with JVM?
Class Area: Stores class-level data, such as class definitions, static variables, method definitions, and metadata related to loaded classes.

Heap: Stores objects and their associated instance variables at runtime.

Stack: Stores local variables and function/method call data (activation records).

Program Counter Register: stores the address of the Java virtual machine instruction currently being executed.

Native method Stack: stores all the native methods used in the application.

6. What is a classloader?
Classloader is the part of Java Runtime Environment during the execution of the bytecode the classloader is responsible for dynamically loading the java classes and interfaces to JVM Because of classloaders Java run time system does not need to know about files and file systems.

7. What Is JRE ?
JRE stands for Java Runtime Environment, it is an installation package that provides an environment to run the Java program on any machine.

8. What is JDK?
JDK stands for Java Development Kit which provides the environment to develop and execute Java programs. JDK is a package that includes two things Development Tools to provide an environment to develop your Java programs and, JRE to execute Java programs or applications.
