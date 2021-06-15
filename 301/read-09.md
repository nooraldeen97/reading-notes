What is functional programming?

Functional programming languages are specially designed to handle symbolic computation and list processing applications. Functional programming is based on mathematical functions. Some of the popular functional programming languages include Lisp, Python, Erlang, Haskell, Clojure, etc.

What is a pure function and how do we know if something is a pure function?

Pure functions is the first term to learn when trying to understand functional programming. Pure function, are functions that return the same result if given the same arguments (they are also referred as deterministic), and they do not cause any observable side effects.

There are several signs to an impure function like :

It uses global variables.
  let PI = 3.14;

  const calculateArea = (radius) => radius * radius * PI;

  calculateArea(10);

  // PI is a global variable that might affect the results if changed 
It reads external files.

const charactersCounter = (text) => `Character count: ${text.length}`;

function analyzeFile(filename) {
let fileContent = open(filename);
return charactersCounter(fileContent);
  }
It relies on a random number generator.

function yearEndEvaluation() {
if (Math.random() > 0.5) {
    return "You get a raise!";
} else {
    return "Better luck next year!";
}
}
It modifying a global object or a parameter passed by reference.
let counter = 1;

function increaseCounter(value) {
counter = value + 1;
}

increaseCounter(counter);
There are many benefits of pure functions like:

The code is easier to test.

We don’t need to mock anything

The code is consistent

Immutability
To say a code is immutable, to mean that it is unchanged or unable to change.

When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

mutable:

var values = [1, 2, 3, 4, 5];
var sumOfValues = 0;

for (var i = 0; i < values.length; i++) {
sumOfValues += values[i];
}

sumOfValues // 15
immutable:

let list = [1, 2, 3, 4, 5];
let accumulator = 0;

function sum(list, accumulator) {
if (list.length == 0) {
  return accumulator;
}

return sum(list.slice(1), accumulator + list[0]);
}

sum(list, accumulator); // 15
list; // [1, 2, 3, 4, 5]
accumulator; // 0
Referential transparency
A function that consistently yields the same result for the same input, is referentially transparent.

pure functions + immutable data = referential transparency

Node JS
A module is a part of a code that represent some functionality, and is made to be used in other code.

So, instead of writing a big code in one file, we divide the code into pieces of modules. Each module will have a single or two things to do, which will make our code easier to be expanded and edit, and highly reusable.

When we wanna use a module inside a file we use require, which will import the module, and enable us to use its functionality.

To use a function inside a module for example the module is called lolo.js and its file is in the home directory and contains a function called doCrazyThings , in a file called taboush.js we write the following code:

First, inside lolo.js we have to specify what things we want to use outside, so we write in its global scope the following: module.export doCrazyThings

After that, inside taboush.js, assign the function of lolo.js in a variable with the use of require: const doIT = require('doCrazyThings')

Now we can use the function inside taboush.js.

Resource
Functional Programming Concepts