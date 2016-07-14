# JavaScript Cheatsheet

Last updated 07/14/2016

## Primitives

Primitives are the JavaScript building blocks.

  - Boolean - `true` or `false`
  - Numbers - integers or floats
  - Strings - text
  - Undefined - value has not been defined
  - Null - intentional absence of an object value
  - Symbol (es6)

## Variables

Container to store data (values)
Shortcuts for storing data

  - Declared using `var`
  - Naming - can't start with a number, can't have spaces, avoid symbols except `_`, `$`, `-`, the name should be descriptive, should be camelCase

## Data Structures

  - Arrays: container for primitives (and other data structures) accessed via index, ordered
  - Objects: key/value pairs, accessed via bracket or dot notation, not ordered


## Programming Paradigms

Procedural vs functional

  - Procedural: JS renders commands in ordered
  - Functional: break apart code/problem logically, generally separate state from behavior, reusable

## Flow Control

Flow control - decides which things run based on specific conditions (order) or loops

Conditionals control the flow of the program
  - if, if-else if-else
  - can be nested

  >remember to fail fast!

Switch statements:

  - We haven't covered these yet, but they can be used to execute multiple blocks of code.

## Loops

  - you can keep running a piece of code for a certain amount of iterations
  - infinite loop - loop that runs forever, stack overflow, no more memory :(

  - for

  - while

  - for in

  - for of

  - do while

## Operators

Math - `+`, `-`, `*`, `/`, `%`, can combine (`++`, `+=`)

Logical - `&&`, `||`

Comparison - `===` (strict), `==` (loose), `>`, `!`, `<`, `>=`, `<=`

## functions

Set of instructions that achieve a specific task defined by code block. Can be defined and then invoked to return some output, can contain parameters (when defined) and arguments (passed in when called/invoked)

  - methods vs functions: method is a function that is contained within an object
  - functions are first class citizens and can be used as arguments (just like primitives and data structures) in JS
  - can have optional
  - functions always return something; if not explicitly set, then it returns `undefined`
  - expression vs declaration

## variable scope

  - range in which a variable can be accessed
  - global and local (function/lexical)
  - global - accesible everywhere; local - accessible only when the function is invoked
  ```
  function foo() {
      var test = "some string"
      function bar() {
        console.log(test);
      }
    }
```
## hoisting

The process by which the computer moves all variable declarations to the top of the applicable scope, so that it never encounters a variable it is unaware of. It's important to note that it does not move the variable assignment to the top of the page.

`var foo = "bar"`

moves declarations (`var: foo`) but NOT assignment (`var foo = bar`)

## callbacks/higher order functions

function can take functions; the function that's passed into the HOF is the callback

asynchronous - different code can run at different times

```
function testing() {
  return ing
}

function test() {
  return "test" + arg
}

var x = testing()
test(x)
```

## string concatenation

Used to join 2 or more strings

```
"test" + "ing"
```

```
"test".concat("ing") // => "testing"
```

you can also use `+=`

## computer science

BigO notation: how developers discuss the complexity of an algorithm as a way to understand how fast a program will run given it's input. Big-O notation deals with the worst case scenario for the algorithm. In other words, if the program may run quickly, but there is a chance it could take a long time given some input, then the Big-O runtime will deal with the longer case

* O(n) - Linear Time
  * Directly related to input size (longer input, longer runtime)
* O(1) - Constant Time
  * Bound by a constant number. Regardless of input size, the runtime stays the statements
* O(n^2) - Quadratic Time
  * A loop that iterates over all items nested within a loop that also iterates over all items

The exponent grows based on the number of nested loops.

A "flogarithm" of a positive number (n) represented by (log(n)) is the number of digits it has.

Factorials - Way worse than quadratix.

[Big O Cheatsheet](http://bigocheatsheet.com/) 
