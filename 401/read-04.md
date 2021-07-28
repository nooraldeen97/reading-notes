## Object-Oriented Programming Concepts
**I learned about:**
Objects
1-Software objects are conceptually similar to real-world objects: they too consist of state and related behavior.<br>
2-An object stores its state in fields (variables in some programming languages) and exposes its behavior through methods (functions in some programming languages).<br>
3- Hiding internal state and requiring all interaction to be performed through an object's methods is known as data encapsulation<br>
4- Bundling code into individual software objects provides a number of benefits, including:<br>
- Modularity: The source code for an object can be written and maintained independently of the source code for other objects<br>
- Information-hiding: By interacting only with an object's methods, the details of its internal implementation remain hidden from the outside world.<br>
- Code re-use: If an object already exists (perhaps written by another software developer), you can use that object in your program<br>
- Pluggability and debugging ease: If a particular object turns out to be problematic, you can simply remove it from your application and plug in a different object as its replacement<br>
## Classes<br>
1- A class is the blueprint from which individual objects are created.<br>
2- class does not contain a main method that's because it's not a complete application; it's just the blueprint<br> for bicycles that might be used in an application<br>
 **Classes**<br>
I learned about:<br>
- Class declaration<br>
- class MyClass {<br>
    // field, constructor, and<br>
    // method declarations<br>
}<br>
1- The class body (the area between the braces) contains:<br>
- all the code that provides for the life cycle of the objects created from the class<br>
- methods to implement the behavior of the class and its objects.<br>
2- You can provide more information about the class, such as the name of its superclass, whether it implements - any interfaces, and so on, at the start of the class declaration.<br>
- class MyClass extends MySuperClass implements YourInterface {<br>
    // field, constructor, and<br>
    // method declarations<br>
}<br>

#### Declaring Member Variables<br>
1- kinds of variables:<br>
Member variables in a class—these are called fields.<br>
Variables in a method or block of code—these are called local variables.<br>
Variables in method declarations—these are called parameters.<br>
2- public modifier—the field is accessible from all classes.<br>
3- private modifier—the field is accessible only within its own class.<br>
4- the first letter of a class name should be capitalized, and<br>
5- the first (or only) word in a method name should be a verb.<br>
#### Defining Methods<br>
1- method declarations components, in order:<br>
- Modifiers—such as public, private.<br>
- The return type—the data type of the value returned by the method, or void if the method does not return a<br> value.<br>
- The method name—the rules for field names apply to method names as well, but the convention is a little <br>different.<br>
- The parameter list in parenthesis—a comma-delimited list of input parameters, preceded by their data types, <br>enclosed by parentheses, (). If there are no parameters, you must use empty parentheses.<br>
- The method body, enclosed between braces—the method's code, including the declaration of local variables, goes here<br>
2- method names should be a verb in lowercase or a multi-word name that begins with a verb in lowercase, followed <br>by adjectives, nouns, etc. In multi-word names, the first letter of each of the second and following words <br>should be capitalized.<br>
3- This means that methods within a class can have the same name if they have different parameter lists<br>
4- Overloaded methods are differentiated by the number and the type of the arguments passed into the method.<br>
5- The compiler does not consider return type when differentiating methods, so you cannot declare two methods with the same signature even if they have a different return type.<br>
#### Providing Constructors for Your Classes<br>
- A class contains constructors that are invoked to create objects from the class blueprint. Constructor <br>declarations look like method declarations—except that they use the name of the class and have no return <br>type
- a constructor is called by the new operator:<br>
- As with methods, the Java platform differentiates constructors on the basis of the number of arguments in the list and their types<br>
- The compiler automatically provides a no-argument, default constructor for any class without constructors.
- You can use access modifiers in a constructor's declaration to control which other classes can call the <br>constructor.<br>
#### Passing Information to a Method or a Constructor<br>
1- You can use any data type for a parameter of a method or a constructor. This includes primitive and reference data types<br>
2- You can use a construct called varargs to pass an arbitrary number of values to a method.<br>
3- to use varargs, you follow the type of the last parameter by an ellipsis (three dots, ...)
4- The name of a parameter must be unique in its scope.<br>
5- A parameter can have the same name as one of the class's fields. If this is the case, the parameter is said to <br>shadow the field. Shadowing fields can make your code difficult to read and is conventionally used only <br>within constructors and methods that set a particular field.<br>
6- Reference data type parameters, such as objects, are also passed into methods by value.<br>

## Binary, Decimal and Hexadecimal Numbers<br>
#### Decimals<br>
-Every digit in a decimal number has a "position", and the decimal point helps us to know which position is which<br>
#### Bases<br>
- there is 10 symbols:<br>
0, 1, 2, 3, 4, 5, 6, 7, 8 and 9<br>
-In binary you count "0,1,..." but then you run out of symbols! So you add 1 on the left and then start again at 0: 10,11 ...<br>
-general rule is Count up until just before the "Base Number", then start at 0 again, but first you add 1 to the number on your left.<br>
#### Binary Numbers<br>
-Binary Numbers are just "Base 2" instead of "Base 10". So you start counting at 0, then 1, then you run out of digits<br>
#### Hexadecimal Numbers<br>
-T-hey look the same as the decimal numbers up to 9, but then there are the letters ("A',"B","C","D","E","F") in place of the decimal numbers 10 to 15.<br>