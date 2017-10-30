# Defining Functions

**In addition to using built in functions that have already been defined, we can define our own functions and use them.**

## Objectives

By the end of this section you should be able to:

- Define a function
- Define a function that returns a value other than `undefined`
- Define a function that defines parameters and returns a value based on those parameters

## Function Definition Syntax

Up until this point we have only called functions that were pre-defined by the JavaScript language. After many digressions, we are now ready to define our own functions, utilizing all (and more) of the JavaScript language features that we have thus far covered.

In JavaScript there are three ways to define a function. With time each of these will become very familiar. For now, just consider this survey of all 3 an introduction, and focus on memorizing the syntax for the first.

The first is called a **function declaration** and follows the following format:

- Use the `function` keyword
- ... followed by the name of the function
- ... followed by opening and closing parenthesis `()`
- ... followed by opening and closing curly braces `{}`

:speak_no_evil: Say out loud, 3 times, the 4 aspects (as described just above) of defining a function with a **function declaration**.
As you already know, after a function has been defined, it can be called with its name followed by parenthesis `()`. Recall that every function returns `undefined` unless specified to return some other value, therefore:

```javascript
function doNothing () {}

let resultOfCallingDoNothing = doNothing();
console.log(resultOfCallingDoNothing); // logs `undefined` to the console
```

When we use **function declarations**, the functions are available for being called anywhere in the file that they were defined, no matter what part of the file they were defined in. This mechanism of making the function available to us in parts of a file that appear before the definition itself is called `hoisting` and regarding function definitions, is only done when using function declarations, the form of defining a function just described. Because of the quality of function declarations being hoisted, the following code works just fine:

```javascript
let resultOfCallingDoNothing = doNothing();
console.log(resultOfCallingDoNothing); // logs `undefined` to the console

function doNothing () {}
```

Technically, function definitions are values of the `object` type, but in a way that is both helpful and confusing, will return that they are of the type `'function'` when passed to the `typeof` function, which is not technically a JavaScript type at all:

```javascript
console.log(typeof(function someFunctionDefinition() {})); // logs `'function'` to the console
```

## Function Expression Syntax

A second way we can define functions is to use a **function expression** which occurs when we assign a function definition to a variable. Function expressions are not hoisted like function declarations, and also, we use the variable name that the function definition is assigned to in order to make the function call:

```javascript
let doNothing = function() {};

console.log(doNothing()); // logs `undefined` to the console
```

## Arrow Function Expression Syntax

A third way we can define functions is using the arrow function expression syntax. This method of defining a function also assigns the function definition to a variable, and, does not involve hoisting. Arrow function expressions are more terse than the other ways of defining functions, and has some subtle differences which you will explore at a later time. Arrow function expressions are a newer addition do the JavaScript language, and in some situations, are incredible advantageous:

```javascript
let doNothing = () => {}

console.log(typeof(doNothing));   // logs `function` to the console
console.log(typeof(doNothing())); // logs `undefined` to the console
```

## Function Definitions vs. Function Calls / Invocations

**It is of the utmost importance to always be able to distinguish between function definitions and function calls (or invocations). Whenever a function is called it results in whatever value the function being called returns. A function definition on the other hand, is a value unto itself, which needs no further evaluation.**

Consider the following:

```javascript
function doNothing () {}

console.log(typeof(doNothing));         // logs `function` to the console
console.log(typeof(doNothing()));       // logs `undefined` to the console

console.log(doNothing === doNothing()); // logs `false` to the console
```

:question: In as much detail as you are able, what is the difference between `doNothing` and `doNothing()` above?

## Returning Values From Functions

As you are well aware from using built in functions, many functions define values other than `undefined`. When writing our own function definitions we can return whatever value we might like by using, somewhere in the **body** of the definition, the `return` keyword, followed by the value we with to return. The **body** of a function definition is the part in between the curly braces, and, is a collection of any JavaScript code. While this description is rather innocuous, a full understanding of it unlocks incredible possibilities in your ability to write functions that can do anything you are able to imagine doing in JavaScript:

```javascript
function makeOne() {
  return 1;
}

console.log(typeof(makeOne));   // logs `'function'` to the console
console.log(typeof(makeOne())); // logs `'number'` to the console
console.log(makeOne());         // logs `1` to the console
```

Commonly, the `return` statement is a result of some more sophisticated operations:

```javascript
function getRemainderOfSeventyDividedByNine() {
  let remainderOfSeventyDividedByNine = 70 % 9;
  return remainderOfSeventyDividedByNine;
}

remainderOfSeventyDividedByNine = getRemainderOfSeventyDividedByNine();
console.log(remainderOfSeventyDividedByNine); // logs `7` to the console
```

## Defining Parameters

You are already used to passing in **arguments** when calling functions. **When defining functions, we can define _parameters_ which will serve as stand in variables inside the function definition which get assigned actual values when the function is called.**

In the following function we define a **parameter** which we call `num`. There is no way to know what the **actual** value of `num` is until the function is actually called, at which point in time, it will be equal to the value that gets passed in.

```javascript
function addOneToNumber(num) {
  return num + 1; // `num` is a variable that will not be assigned an actual value until `addOneToNumber` is called
}

console.log(addOneToNumber(11)); // logs `12` to the console
```

The fact that we can define parameters, which could be any value depending on how the function is called, is incredibly helpful and allows us to define a single function to be called with a variety of values to do a variety of operations:

```javascript
function addOneToNumber(num) {
  return num + 1; // `num` is a variable that will not be assigned an actual value until `addOneToNumber` is called
}

console.log(addOneToNumber(11)); // logs `12` to the console
console.log(addOneToNumber(12)); // logs `13` to the console
console.log(addOneToNumber(13)); // logs `14` to the console
```

## Defining Multiple Parameters

Functions can be defined with as many parameters as we would like:

```javascript
function addToLastElement(numberToAddToLastElement, numbers) {
  let lastNumber = numbers.pop();
  return lastNumber + numberToAddToLastElement;
}

let numbers = [1, 2, 3];
let lastNumberPlusFour = addToLastElement(4, numbers);

console.log(lastNumberPlusFour); // logs `7` to the console
```

It is very worth noting that because we passed in an array to `lastNumberPlusFour`, and, because assigning arrays to variables (in this case `numbers`) only means that we add an additional label onto the one unique array, it turns out that the above code has modified the `numbers` array defined outside the function body:

```javascript
function addToLastElement(numberToAddToLastElement, numbers) {
  let lastNumber = numbers.pop(); // `numbers` does not make a new array, but only references an already existing one, thus modifying it
  return lastNumber + numberToAddToLastElement;
}

let numbers = [1, 2, 3];
let lastNumberPlusFour = addToLastElement(4, numbers);

console.log(lastNumberPlusFour); // logs `7` to the console
console.log(numbers);            // logs `[1, 2]` to the console
```

## Conclusion

We can define our own functions which can, should we choose, return values that we define, and/or, have defined parameters on whose values will be determined when the function is called and passed in arguments.

This is really only the very beginning of utilizing functions. In the next section we will turn to a very important principle, which is to house several smaller functions in smaller functions.

Before continuing, be sure that you can do the following:

- Define a function
- Define a function that returns a value other than `undefined`
- Define a function that defines parameters and returns a value based on those parameters

## Table of Contents

### Basic Training Materials

- [Introduction](../README.md)
- [JavaScript and Modern Web Development](modern_web_development.md)
- [Dev Environment Setup](setup.md)
- [Introduction to Functions](intro_to_javascript_functions.md)
- [Basic Use of Functions](basic_use_of_functions.md)
- [JavaScript Types Crash Course](type_crash_course.md)
- [Functions that Make Values](functions_that_make_values.md)
- [Variables](variables.md)
- [String Methods](string_methods.md)
- [Introduction to Arrays](intro_to_arrays.md)
- *Defining Functions*
- [Leveraging Multiple Functions](leveraging_multiple_functions.md)
- [Next Steps](next_steps.md)

### Advanced Content

- [Passing Functions as Arguments](passing_functions_as_arguments.md)
- [Higher Order Array Methods](higher_order_array_methods.md)

### Appendix

- [Reference and Further Study](reference.md)
