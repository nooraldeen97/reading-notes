## packeges 
**packege is the same as directory which contain java classes , we import it and name what we want and use from other libraries.**

***package declarations must be the first statements*** <br>
***after importing a package you can specify classes from that package***<br>
***For small programs it's common to omit package declaration, although it is not recommended.***<br>
**The wildcard character (*) is used to specify that all classes with that package are available to your program.**<br>
***you can specify the exact class that you want to use instead of ***<br>

Common imports:<br>
import java.awt.*; Common GUI elements.<br>
import java.awt.event.*; The most common GUI event listeners.<br>
import javax.swing.*; More common GUI elements. Note "javax".<br>
import java.util.*; Data structures (Collections), time, Scanner, etc classes.<br>
import java.io.*; Input-output classes.<br>
import java.text.*; Some formatting classes.<br>
import java.util.regex.*; Regular expression classes.<br>


***imports doesn't make the file larger***<br>
**using * in the import prevents accidentally defining classes with names that conflict with the standard library names**<br>
**import with * doesn't include any of the subpackages**<br>
**Static imports in Java 5 leads to name pollution and confusion about which class constants come from.**<br>

<hr>

## A Guide to Java Loops

I have learned about:<br>
the types of loops that we can find in Java:<br>
Simple for loop: incrementing and evaluating a loop counter.<br>
Enhanced for-each loop: for each element<br>
While loop: while a condition is true<br>
Do-While loop: the first condition evaluation happens after the first iteration of the loop.<br>
We know that each loop serves a particular purpose given a suitable use case.