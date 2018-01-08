# Variables

A variable stores a value for later use.  Two things to note.  This stored value may both (1) have any type and (2) be used many times.  

## Objectives

After completing this section, you should:

- Declare variables
- Assign values to variables
- Reassign new values to variables
- Assign a variable's value to other variables

## Declaring Variables

To store a value, we must first declare a variable.  Only after declaration can a value be stored.

How to declare a variable?  First use the keyword `let`.  Follow with the variable's name.  Look at the simple example below.  

```javascript
let variableName;
```

Above, the declared variable's name is `variableName`.  Please note that a value was NOT assigned to `variableName`.

### Variable Analogy

Let's imagine a variable as a box.  Two important points.

(1). This box can contain any kind of thing.  We'll discuss this more later.

(2).  This box has a label.  In the previous example, the label read `variableName`.  Best practice is to give a label which helps understand the box's contents.  Just like in real life.

## Variables Declared Without Values

In the previous example, the declared variable `variableName` was **not** assigned a value.  In these cases, JavaScript will automatically assign that declared variable the value `undefined`.

```javascript
let name;

console.log(name); // logs `undefined` to the console
```

### Note
In the example above, notice that the variable `name` passed into `console.log` did **not** have quotes.  By definition, any value surrounded by quotes is a string -- NOT a variable.

```javascript
let name;
console.log(typeof(name));    // logs `'undefined'` to the console
console.log(typeof('name'));  // logs `'string'` to the console
console.log(name === 'name'); // logs `false` to the console
```

## Let, Var, and Const

Need a variable?  `let` is not the only game in town.  

Two more keywords exist for declaring variables -- `var` and `const`.  Discussion of these other two keywords is outside the scope of this intro class.  

Here are the recommended guidelines:

> -- Use `let` as your default for declaring variables
> -- Use `const` if and only if certain the variable's value will NEVER change.
> -- Use `var` after gaining a solid understanding of **Global Scope**.  But please note, probably best still to simply use `let`.

:star: In the text editor, declare 4 different variables. The variables may have any name.

:question: What happens if you try to declare a variable that has a name like `4` or `16`?

:question: What happens if you try to declare a variable that has a name that looks like some of the other built in words like `let`, `true`, `undefined`?

## Assigning Values to Variables

Generally, a declared variable is also assigned a corresponding value.  When **assigning** values, use the **assignment operator** -- a single equal sign (`=`).

On the left goes the keyword `let` and the variable's name.  On the right goes the value to be stored.  Below is a simple example.

```javascript
let instructorName
instructorName = 'justin';

console.log(instructorName) //==> 'justin'
```

On the first line, a variable named `instructorName` is declared. Then `instructorName` is assigned a value.

In real life, these two steps are done in one line.

```javascript
let instructorName = "justin";
console.log(instructorName) //==> 'justin'
console.log(typeof instructorName) //==> 'string'

let age = 74;
console.log(age) //==> 74
console.log(typeof age) //==> 'number'

```

:star: Declare two variables, one called `aNumber`, and another called `anotherNumber`.  Assign some value of type `number` to each. Then, log to the console the result of adding the 2 number-containing variables.

:star: In the code below, 3 variables have been declared. Assign values to each of them so that they contain values akin to their names and cause the final `console.log` to log `true`.

```javascript
let two;
let three;
let twoIsGreaterThanThree;

console.log(twoIsGreaterThanThree); // should log `true` to the console
```

## Reassigning Values to Variables

**Variables with assigned values can be assigned new values.** Analogous to taking something out of a labeled box and putting in something different.

```javascript
let name = 'Rowan';
console.log(name); // logs 'Rowan' to the console

name = 'Ro';       // <--- Assigning a new value to the variable
console.log(name); // logs 'Ro' to the console
```

An exception to this rule is if you declare your variable with the `const` keyword, which will make the variable **read only**.

```javascript
const name = 'Rowan';
name = 'Ro' // This will cause your code to throw an error
```

### Variable Naming
Do not use cryptic variable names.  **legible is better than clever**.

Over time, your ability to name variables will improve.  In the meantime, write code that reads like English.  Use simple, descriptive variable names.

**Variable names are chosen by programmers and we can only hope that they accurately describe the value assigned to the variable. Watch out.**

```javascript
let name = 8;
let food = 'staircase';
let theTruth = false;
let big = 0;
big = 'small';
big = null;
big = food;
```

## Assigning Variables to Other Variables

One variable may also be assigned to another.  For today's purposes, let's discuss only values of the types `string`, `number`, `boolean`, `undefined` and `null`.

The second variable's value is an identical copy to the first.  

Please note: changing the first variable's value will NOT change the second's.  Making this mistake is common.

```javascript
let first = 35;
let second = first;

console.log(first);  //==> 35
console.log(second); //==> 35

first = 83;
console.log(second); //==> 35
console.log(first);  //==> 83
```

## Conclusion

A variable is like a labeled box.  This box may contain any value of any type -- or no value.   Examples include values created from operations and values stored in other variables.

Before continuing, be sure that you can:

- Declare variables
- Assign values to variables
- Reassign new values to variables
- Assign values already stored in variables to other values
