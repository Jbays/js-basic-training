# Variables

In JavaScript, a variable stores a value of any type so that it can be used later in a program, potentially many different times. Variables can store values that are the result of sophisticated operations, also allowing programmers a way to indicate what a particular value ought to represent.

## Objectives

By the time you complete this section you should be able to:

- Declare variables
- Assign values to variables
- Assign values returned from functions to variables
- Reassign new values to variables
- Assign values already stored in variables to other variables

## Declaring Variables

**In JavaScript, a variable stores a value of any type so that we can use it later in our program. In order to use a variable we must ffirst _declare_ it, after which we can _assign_ a value to it.**

In order to **declare** a variable in JavaScript, we use the `let` keyword, followed by the name we would like to give to the variable. In this example we declare a new variable called `name`:

```javascript
let name;
```

You can think of a variable as a box with a label on it. The box can contain any kind of thing, and the label (hopefully, though not necessarily) will help us understand what is inside the box.

When we first **declare** a variable it is automatically **assigned** the value `undefined`:

```javascript
let name;

console.log(name); // logs `undefined` to the console
```

Note that when we pass the **variable** `name` into `console.log` above, we do **not** surround it with quotes of any kind. Remember that values surrounded by quotes refer to **strings**. Variables, on the other hand, might "contain" a value of any type.

```javascript
let name;
console.log(typeof(name));    // logs `'undefined'` to the console
console.log(typeof('name'));  // logs `'string'` to the console
console.log(name === 'name'); // logs `false` to the console
```

> In addition to **declaring** a variable with the `let` keyword, we can also use the `const` or `var` keywords. We will avoid a detailed discussion of the implications for declaring variables with each of these 3 different keywords here, but for now:

> - Use `let` as your default for declaring variables
> - If you know for certain that your variable will never be changed (more on this below) then use `const`
> - Use `var` after you understand what **Global Scope** means, and in the meantime (although this isn't totally accurate) consider it as equivalent to `let`

:star: In the text editor, declare 4 different variables, giving them any name you wish.

:question: What happens if you try to declare a variable that has a name like `4` or `16`?

:question: What happens if you try to declare a variable that has a name that looks like some of the other built in words like `let`, `true`, `undefined`?

## Assigning Values to Variables

After **declaring** a variable, we can **assign** a value of any type to it. When **assigning** values to a variable we use the **assignment operator** which is a single equal sign (`=`), placing the variable on the left hand side and the value we wish to "store" in the variable on the right. In the following example, we declare the variable `name` and then assign a value of type `string` to it:

```javascript
let name;
name = 'Rowan';

console.log(name);         // logs `'Rowan'` to the console
console.log(typeof(name)); // logs `'string'` to the console
```

As a matter of convenience, JavaScript allows us to both **declare** and **assign** a variable on the same line, thus:

```javascript
let name = 'Rowan';
let age = 1;
```

:star: Declare two variables, one called `aNumber`, and another called `anotherNumber`, and assign some value of type `number` to each of them. Then, log the result of adding the 2 number-containing variables in the console.

## Assigning Values Returned From Functions to Variables

Values returned from calling functions can be assigned to variables, just like any other value.

```javascript
let largestNumber = Math.max(5, 7, 2);
console.log(largestNumber); // logs `7` to the console
```

Storing returned values can be helpful in making our code easy to read and reason about, for example, compare the following two blocks of code:

```javascript
console.log(typeof(String(Math.max(0, 3, 1))) === typeof('number'));
```

Here's a refactor that makes some variable assignments to make the code easier to read and reason about:

```javascript
let largestNumber = Math.max(0, 3, 1);
let largestNumberString = String(largestNumber);

console.log(typeof(largestNumberString) === typeof('number')); // logs `true` to the console
```

We *could* make a choice to use even more variables:

```javascript
let largestNumber = Math.max(0, 3, 1);
let largestNumberString = String(largestNumber);
let typeofLargestNumberString = typeof(largestNumberString);

let someString = 'number';
let typeofSomeString = typeof(someString);

let typeofSomeStringIsEqualTotypeofLargestNumberString = typofSomeString === typeofLargestNumberString;
console.log(typeofSomeStringIsEqualTotypeofLargestNumberString); // logs `true` to the console
```

But probably you will agree this last section of code is not so nice. Over time you will develop a keen sense for when to use variables and when not to based on personal experience. In the meantime, this author recommends you aim to write code that reads like English, which means, using descriptive variable names more often than not.

> Don't make the mistake of thinking that short variable names saves you time or makes your code run faster, it doesn't. Cryptic code will cost everyone dearly who has to come back and figure out what your code is doing later. While it is fun at times to write the most dense and elegant solution, **legible is better than clever.**

:star: In the code below, 3 variables have been declared. Assign values to each of them so that they contain values akin to their names and cause the final `console.log` to log `true`.

```javascript
let two;
let three;
let twoIsGreaterThanThree;

console.log(twoIsGreaterThanThree); // should log `true` to the console
```

## Reassigning Values to Variables

**Variables that have already been assigned values can be assigned new values.** You can think of this as analogous to taking something out of a labeled box and putting something different in it.

```javascript
let name = 'Rowan';
console.log(name); // logs 'Rowan' to the console

name = 'Ro';       // <--- Assigning a new value to the variable
console.log(name); // logs 'Ro' to the console
```

An exception to this rule is if you declare your variable with the `const` keyword, which will make the variable **read only**.

```
const name = 'Rowan';
name = 'Ro' // This will cause your code to throw an error
```

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

## Assigning Variable Values to Other Variables

**We can assign values stored in one variable to another variable.**

The results of doing this vary depending on which type the value is. For the purposes of this section, we will speak about values of the types `string`, `number`, `boolean`, `undefined` and `null` (that is, values that are not of the `object` type).

Assigning a variable value to another value is like saying "Give me something identical to whatever is in that box so I can put that identical copy in this new box." This means that after assigning a variable value to another variable, reassigning one of the variables does not affect the other, in the same way that opening up one of our two boxes doesn't affect the other box at all. Thus:

```javascript
let aNumber = 3;
let anotherNumber = aNumber;

console.log(aNumber);                   // logs `3` to the console
console.log(anotherNumber);             // logs `3` to the console
console.log(aNumber === anotherNumber); // logs `true` to the console

aNumber = 5;

console.log(aNumber);                   // logs `5` to the console
console.log(anotherNumber);             // logs `3` to the console
console.log(aNumber === anotherNumber); // logs `false` to the console
```

## Conclusion

A value of any type can be assigned to a variable, which acts like a labeled box, containing that value. This included values that are returned from functions, values that are created from operations like, and values that are already stored in other variables.

Before continuing, be sure that you can:

- Declare variables
- Assign values to variables
- Assign values returned from functions to variables
- Reassign new values to variables
- Assign values already stored in variables to other values

## Self Assessment

:question: What will happen on each line when you try to run the following code? Why?

```javascript
const biggest = Math.max(1, 3, 4);
let newBiggest = 12;

biggest = newBiggest;

console.log(biggest);
```

## Next Steps

Now that we know how to store values in variables, including values that functions return, we can return to our discussion of calling functions. Next we will focus on more sets of built in functions so as to increase our fluency in the tools JavaScript provides. These next functions are a of a special kind that can operate "directly" on values (as you'll see), that are called **methods**.
