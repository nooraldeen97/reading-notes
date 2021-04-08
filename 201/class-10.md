To find the source of an error, it helps to know how scripts are processed, The JavaScript interpreter uses
the concept of execution contexts, There is one global execution context; plus, each function creates a new
new execution context. They correspond to variable scope.

**EXECUTION CONTEXT:**
Every statement in a script lives in one of three execution contexts:
**-GLOBAL CONTEXT** 
**-function context**
**EVAL CONTEXT (NOT SHOWN)**

**VARIABLE SCOPE:**
The first two execution contexts correspond with the notion of scope:
**-GLOBAL SCOPE**
**-FUNCTION-LEVEL SCOPE**

If a JavaScript statement generates an error, then it throws an exception.
At that point, the interpreter stops and looks for exception-handling code.

you havr to deal with Errors that you might meet by :
**1: DEBUG THE SCRIPT TO FIX ERRORS:** Debugging is about deduction: eliminating potential causes of an error.
**2: HANDLE ERRORS GRACEFULLY.**

The JavaScript console will tell you when there is a problem with a script,
where to look for the problem, and what kind of issue it seems to be.

You can pause the execution of a script on any line using breakpoints. Then you can check the
values stored in variables at that point in time.