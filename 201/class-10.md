To find the source of an error, it helps to know how scripts are processed, The JavaScript interpreter uses
the concept of execution contexts, There is one global execution context; plus, each function creates a new
new execution context. They correspond to variable scope.

**EXECUTION CONTEXT:**
Every statement in a script lives in one of three execution contexts:<br>
**-GLOBAL CONTEXT** <br>
**-function context** <br>
**EVAL CONTEXT (NOT SHOWN)** <br>
**VARIABLE SCOPE:** <br>

The first two execution contexts correspond with the notion of scope: <br>
**-GLOBAL SCOPE** <br>
**-FUNCTION-LEVEL SCOPE** <br>

If a JavaScript statement generates an error, then it throws an exception. <br>
At that point, the interpreter stops and looks for exception-handling code.<br>

you havr to deal with Errors that you might meet by :<br>
**1: DEBUG THE SCRIPT TO FIX ERRORS:** Debugging is about deduction: eliminating potential causes of an <br>error.<br>
**2: HANDLE ERRORS GRACEFULLY.**<br>

The JavaScript console will tell you when there is a problem with a script,<br>
where to look for the problem, and what kind of issue it seems to be.<br>

You can pause the execution of a script on any line using breakpoints. Then you can check the<br>
values stored in variables at that point in time.<br>