## Java Primitives versus Objects

I learned about:<br>
1- java has 2 fold type system consisting of:<br>
#### primitives such as:<br>
int<br>
boolean<br>
#### reference types such as:<br>
Integer<br>
Boolean<br>
2- Every primitive type corresponds to a reference type.<br>
3- rapper classes are immutable (so that their state can't change once the object is constructed) and are final (so that we can't inherit from them).<br>
autoboxing: converting a primitive type to a reference<br>
unboxing: converting a reference type to a primitive<br>
4- Single Item Memory Footprint:<br>
#### primitive types:<br>
boolean – 1 bit<br>
byte – 8 bits<br>
short, char – 16 bits<br>
int, float – 32 bits<br>
long, double – 64 bits<br>
#### reference types:<br>
Boolean – 128 bits<br>
Byte – 128 bits<br>
Short, Character – 128 bits<br>
Integer, Float – 128 bits<br>
Long, Double – 192 bits<br>
5- The reference types are objects, they live on the heap and are relatively slow to access.<br>
6- primitive type live in the stack and hence are accessed fast.<br>
7- Memory Footprint for Arrays.<br>

8- arrays of the primitive types long and double consume more memory than their wrapper classes Long and Double
9- single-element arrays of primitive types are almost always more expensive (except for long and double) than <br>the corresponding reference type.<br>
10- For the wrapper classes, the default value is null.<br>
11- the reference types might acquire a value (null) that in some sense doesn't belong to their domains which may cause errors if they didn't get uninitialized.<br>
12- Java language specification doesn't allow usage of primitive types in the parametrized types (generics), in the Java collections or the Reflection API.<br>

## Exceptions in Java<br>
I learned about:<br>
What Is an Exception?<br>
- An exception is an event, which occurs during the execution of a program, that disrupts the normal flow of - the program's instructions.<br>
- throwing an exception is Creating an exception object and handing it to the runtime system.
- call stack: the ordered list of methods that had been called to get to the method where the error occurred.
call stack<br>
- exception handler: a block of code that can handle the exception<br>
- when the runtime system exhaustively searches all the methods on the call stack without finding an appropriate exception handler it terminates the program<br>
terminates<br>
The Catch or Specify Requirement<br>
a code that might throw certain exceptions must be enclosed by either of the following:<br>
- A try statement that catches the exception.<br>
- A method that specifies that it can throw the exception. The method must provide a throws clause that lists the exception,
Not all exceptions are subject to the Catch or Specify Requirement.<br>

The Three Kinds of Exceptions
- checked exception: a well-written application should anticipate and recover from, All exceptions are checked exceptions, except for those indicated by Error, RuntimeException, and their subclasses<br>
- error: exceptional conditions that are external to the application, and that the application usually cannot anticipate or recover from<br>
- runtime exception: exceptional conditions that are internal to the application, and that the application usually cannot anticipate or recover from, indicate programming bugs, such as logic errors or improper use of an API.<br>
<hr>
Errors and runtime exceptions are collectively known as unchecked exceptions.<br>

- Catching and Handling Exceptions<br>
- FileWriter constructor: If the file cannot be opened, the constructor throws an IOException.<br>

- ArrayList class's get method, which throws an IndexOutOfBoundsException if the value of its argument is too small (less than 0) or too large (more than the number of elements currently contained by the ArrayList).<br>
- he compiler prints an error message about the exception thrown by the FileWriter constructor. However, it <br>does not display an error message about the exception thrown by get the reason is:
- IOException, is a checked exception.<br>
- IndexOutOfBoundsException, is an unchecked exception.<br>
Using Scanner to read in a file in Java
I learned about:
- Objects of type Scanner are useful for breaking down formatted input into tokens and translating individual tokens according to their data type
- White space characters include blanks, tabs, and line terminators
- close is a method to close it when the Scanner is done.
- To use a different token separator, invoke useDelimiter()
- The ScanSum example reads a list of double values and adds them up

