# Functions that Make Values

As discussed earlier, while all functions **do** something, calling functions can also result in that function **making** something new.

## Objectives

By the time you complete this section you should be able to:

- Speak accurately about functions **returning** values when **called**
- Understand that all functions in JavaScript return values
- Use a few built in functions (`typeof`, `String`, `Math.min`, and `Math.max`) to return new values

## Terminology for Functions That Make New Things

**When we talk about functions that "make new things" we use the more accurate technical language that _calling_ functions _return_ new values.**

In the real world it is perfectly natural to say "When I **call** someone they will **return** my call," and thinking about function **calls** and their resulting **return** values in this way can prove helpful.

Here's an example using a built-in function that we have not yet discussed: `typeof`. The `typeof` function takes a single **argument**, and when **called** returns a **string value** that indicates the **type** of the value that was **passed in.** Here we will **call** `typeof`, which will **return** a new value, and will **pass** that new value as an **argument** into `console.log`:

```javascript
console.log(typeof(8));                   // logs `'number'` to the console
console.log(typeof('gimme a new value')); // logs `'string'` to the console
console.log(typeof(true));                // logs `'boolean'` to the console
console.log(typeof(undefined));           // logs `'undefined'` to the console
console.log(typeof(null));                // logs `'object'` to the console
```

## All Functions Return New Values

**In JavaScript, all functions return a new value when called. When programmers create functions that they don't intend to return a new value, that function will return `undefined`. Returned values, like any value, can be passed into functions.**

One such function that is not intended to return a new value is `console.log`. However, since **every function call in JavaScript returns a value**, we should not be surprised to see that `console.log` returns `undefined`. Here we call `console.log`, passing its newly created return value into another call to `console.log`.

```javascript
console.log(console.log()) // logs `'undefined'` to the console
```

## A Few Built In Functions Returning New Values

In addition to `console.log` there are many other built in functions in JavaScript. Just like fluency in operators will allow us to do more in our programming, fluency with built in functions will also.

Let's explore a few built in functions that unlike `console.log`, return values. This will give us an opportunity to practice understanding return values and will give us more practice evaluating expressions and using comparison operators.

### The Built In `String` Function

The built in function `String` takes a single argument of any type and returns a string representation of it:

```javascript
console.log(String(8));         // logs `'8'` (as a string) to the console
console.log(String(undefined)); // logs `'undefined'` (as a string) to the console
```

:star: Use the text editor and `console.log` to find out what happens when you pass a value that is already type `string` to the `String` function.

:star: Practice evaluating expressions (in your head) and evaluating comparison operators by trying to answer, without using a text editor, what will each of the following lines of code would log to the console if run. After making your best effort, copy and paste the code into the editor and run it to see if you were correct. If you were not, spend more time understanding why it runs the way it does.

```javascript
console.log(String(1234));
console.log(typeof(String(null)));
console.log(String(true) === true);
console.log(String(false) === 'false');
console.log(String(console.log('Not undefined')) === 'undefined');
console.log(String(console.log('Not undefined')) !== 'Not undefined');
```

### The Built In Math.max and Math.min Functions

The `Math.min` and `Math.max` functions both take any number of numerical arguments and return a value of the `number` type for whichever was the smallest or largest number passed in, respectively.

```javascript
console.log(Math.max(2, 5, 8, 1, 3)); // logs `8` to the console
console.log(Math.min(2, 5, 8, 1, 3)); // logs `1` to the console
```

:star: Practice evaluating expressions (in your head) and evaluating comparison operators by trying to answer, without using a text editor, what will each of the following lines of code would log to the console if run. After making your best effort, copy and paste the code into the editor and run it to see if you were correct. If you were not, spend more time understanding why it runs the way it does.

```javascript
console.log(Math.max(8, 7, 9) === 9);
console.log(Math.min(8, 7, 9) === '7');
console.log(Math.min(8, 7, 9) === Math.max(3, 7, 4));
console.log(String(Math.min(8, 7, 9)) === '9');
console.log(Math.max(0) >= Math.min(0));
console.log(typeof(Math.max(0)) === 'number');
console.log(typeof(String(Math.max(0))) === typeof(String('number')));
```

## Conclusion

All JavaScript functions, when called, return a value. Even functions that are not intended to be used for their return values return `undefined`. Returned values, just like any other value, can be passed into functions.

Before continuing, be sure that you can:

- Speak accurately about functions **returning** values when **called**
- Understand that all functions in JavaScript return values
- Use a few built in functions (`String`, `Math.min`, `Math.max`) to return new values

## Self Assessment

:speak_no_evil: Making sure to use terms like **return**, read the following lines of code out loud:

```javascript
console.log(String(console.log('Not undefined')) === 'undefined');
```

:star: Write a one line program that converts both a number and a boolean to a string, and then logs to the console which is greater than the other.

:star2: Find out why your program just written behaves in the way that it does.

## Next Steps

Before continuing further into using functions, and eventually, defining our own, we need to take a brief segue into **variable** declaration, which will allow us to store values, including those returned from functions, so that we can use them in a variety of locations in our programs.
