# Introduction to Arrays

**Arrays are an ordered collections of values, which can be of any type.**

## Objectives

By the time you complete this section you should be able to:

- Create **arrays**
- Get the length of an **array**
- Access an element of an **array** at a given index
- Say some meaningful things about how assigning **arrays** to variables is different than assigning strings to variables
- Use several basic **array** methods

## Creating Arrays

Technically, **arrays** are a value of the `object` type (the implications of this we will largely avoid for the time being). The most common way to create an array is with the square brackets (`[]`), placing values of any type inside of the brackets, separated by a comma. The values inside of an array are called **elements**. Every array has a special **property** called `length`, which, much like a method, can be accessed using dot notation on the array value itself. The `length` property will return a new value of the `number` type which is the number of **elements** in the array.

Here we create an array of letters, where each **element** is a value of the `string` type, and then access its `length` property:

```javascript
let letters = ['a', 'b', 'c', 'd'];
console.log(letters.length); // logs `4` to the console
```

Each **element** in an array has an **index** indicating its position, starting at `0`, just like characters in a string. An **element** at a given **index** within an array can be accessed by using (yet again) the square brackets (`[]`) after the array (or variable containing the array), inserting the **index** of the value that we would like access to. Thus:

```javascript
let letters = ['a', 'b', 'c', 'd'];
let firstLetter = letters[0];
let secondLetter = letters[1];

console.log(firstLetter);  // logs `'a'` to the console
console.log(secondLetter); // logs `'b'` to the console
```

As stated above, arrays can contain values of different types:

```javascript
let valuesOfDifferentTypes = ['string', 1, true, undefined, null];

console.log(typeof(valuesOfDifferentTypes[0])); // logs `'string'` to the console
console.log(typeof(valuesOfDifferentTypes[1])); // logs `'number'` to the console
console.log(typeof(valuesOfDifferentTypes[2])); // logs `'boolean'` to the console
console.log(typeof(valuesOfDifferentTypes[3])); // logs `'undefined'` to the console
console.log(typeof(valuesOfDifferentTypes[4])); // logs `'null'` to the console
```

Arrays can also contain inner arrays:

```javascript
let collections = [['a', 'e', 'i', 'o', 'u'], [1, 2, 3], [true, false]];
let vowels = collections[0];
let nums = collections[1];
let booleans = collections[2];

console.log(vowels[0]);                          // logs `'a'` to the console
console.log(nums[1]);                            // logs `2` to the console
console.log(booleans[1]);                        // logs `false` to the console

console.log(vowels.length === booleans.length);  // logs `false` to the console
console.log(collections.length === nums.length); // logs `true` to the console
```

:star: Copy and paste the following snippet into a text editor and modify `collection` so that both of the `console.log`s return `true` (you might have to investigate what the index is for a character that is not inside a string):

```javascript
let word = 'code';
let collection = [];

console.log(collection.length === word.length);
console.log(collection[2] === word.indexOf('a'));
```

## Array Methods: `push` and `pop`

Arrays, just like strings, have a set of **methods** that can be used directly on array values. The `push` method adds the value passed into it to the end of the array that it was called on:

```javascript
let nums = [1, 2, 3];
console.log(nums.length); // logs `3` to the console

nums.push(4);
console.log(nums.length); // logs `4` to the console
console.log(nums);        // logs `[1, 2, 3, 4]` to the console
```

The `pop` method removes the last value of the array that it was called on and returns the value of the popped off element:

```javascript
let letters = ['w', 'x', 'y', 'z'];
console.log(letters.length);            // logs `4` to the console

let lastLetter = letters.pop();
console.log(lastLetter);                // logs `'z'` to the console
console.log(letters.length);            // logs `3` to the console

let secondToLastLetter = letters.pop(); // logs `'y'` to the console
console.log(letters.length);            // logs `2` to the console
```

## Array Variables are Labels, Not Boxes With Labels (advanced)

Recall from earlier the claim that assigning values (that are not of the `object` type) is like adding them to a box with the variable name being the label on the box. Also remember that when we assign a variable value to another variable, that in our analogy, we now have two different boxes each with different labels and distinct values. Thus, as a reminder:

```javascript
let a = 12;
let b = a;

console.log(b);       // logs `12` to the console
console.log(a === b); // logs `true` to the console

a = 5;
console.log(b);       // logs `12` to the console
console.log(a === b); // logs `false` to the console
```

Arrays, being a value of the `object` type behave rather differently. **Every single value of the `object` type, even if they look similar, is an entirely unique value.** Therefore, when we assign a value that is of the type `object` (for instance, an array), to a variable, we can think of the variable as simply being a label on the value, as opposed to a box with a label. Furthermore, if we assign this variable value to another variable, the new variable is simply an additional label on the value, and **not** a new and second box with an identical value inside of it. Thus:

```javascript
let nums = [1, 2, 3];
let sameNums = nums;

nums.push(4);
console.log(nums);                          // logs `[1, 2, 3, 4]` to the console
console.log(sameNums);                      // logs `[1, 2, 3, 4]` to the console

sameNums.pop();
console.log(nums.length);                   // logs `3` to the console

console.log(nums === sameNums);             // logs `true` to the console

let looksLikeNumsButIsnt = [1, 2, 3];
console.log(looksLikeNumsButIsnt === nums); // logs `false` to the console
```

## Array Method: `reverse`

The array method `reverse` reverses the order of the array it was called on, and also returns the reversed array:

```javascript
let nums = [1, 2, 3, 4, 5];
let reversedNums = nums.reverse();

console.log(reversedNums[0]); // logs `5` to the console
console.log(nums);            // logs `[5, 4, 3, 2, 1]` to the console
```

## Array Method `join` and the String Method `split`

In the last section we mentioned the string method `split` which takes a string and returns a new array whose elements are the sections of a string resulting from splitting the string into section at a given character. Recall:

```javascript
let sentence = ['This is a sentence.'];
let words = sentence.split(' ');

console.log(words); // logs `['This', 'is', 'a', 'sentence']` to the console
```

The array method `join` is complementary to the string method `split`: it takes an array of string characters and **joins** it into a single value of the `string` type with each element in the array being joined together with the passed in character. Thus:

```javascript
let words = ['This', 'is', 'a', 'sentence'];
let sentence = words.join(' ');
console.log(sentence); // logs `'This is a sentence'` to the console
```

Very commonly when using either `split` or `join`, we simply want to convert a string to be an array where each and every character is one of the elements, or, convert an array to be a string where every character is one of the elements with no intervening characters. In both of these situations we utilize the empty string:

```javascript
let word = 'hello';
let characters = word.split('');
console.log(characters);          // logs `['h', 'e', 'l', 'l', 'o']` to the console

let joined = characters.join('');
console.log(joined === word);     // logs `true` to the console
```

It is common also to want to convert a string to an array to utilize array methods not available on strings, and then, convert the array back to a string. Here's an example that leverages the array method `reverse` that is not available to us on strings:

```javascript
let word = 'code';
let letters = word.split('');
let reversedLetters = letters.reverse();
let reversedWord = reversedLetters.join('');

console.log(reversedWord); // logs `edoc` to the console
```

While we have been focusing very much on storing values in variables, recall that this is often a choice, and sometimes, rather than store every intermediate value in a variable, we may wish simply to perform multiple operations at a time. Here is the example from above in a more concise way. One way is not better than the other, there is simply a trade off between how concise vs. how legible the code is, and again, a sense of which is better will grow naturally with experience:

```javascript
let reversedCode = 'code'.split('').reverse().join('');
console.log(reversedCode); // logs `'edoc'` to the console
```

Here is another example where we utilize the string method `toUpperCase` that is not available to us on arrays:

```javascript
let states = ['ca', 'ny', 'or'];
let upperCaseStates = states.join(' ').toUpperCase().split(' ');

console.log(states); // logs `['CA', 'NY', 'OR']` to the console
```

## Many More Array Methods

There are a wealth of methods available on arrays, and while you should not take the time presently to learn them all, knowing which tools you have at your disposal is helpful when considering how to approach a problem. With that in mind, check out [the docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Methods_2) focusing in particular for the time being on the more basic **Mutator** and **Accessor** methods.

## Summary

Arrays are ordered sequences of elements which can be accessed by their indexes and which come with a wealthy selection of methods. Arrays (as values of the `object` type) act differently than primitive values like strings and booleans when assigned to variables, since arrays are, even when they look identical, in fact unique values, every one.

Before continuing be sure that you can:

- Create arrays
- Get the length of an array
- Access an element of an array at a given index
- Say some meaningful things about how assigning arrays to variables is different than assigning strings to variables
- Use several basic array methods

## Self Assessment

:star: Copy and paste the following into a text editor. Use string and array methods as necessary to make the `console.log`s return `true`:

```javascript
let order = 'Now!';
let question = 'Now?';

console.log(order.endsWith('.'));
console.log(question.endsWith('.'));
console.log(order === question);
```

## Next Steps

Now that we have completed the digression into string methods, arrays, and array methods, your vocabulary around fundamental JavaScript language features is growing, and you're closer to being able to solve any number of programming challenges. Now we are ready to return to our discussion of functions, learning how to create our own custom function definitions, which can utilize any (and more) of the language features we have thus far covered.
