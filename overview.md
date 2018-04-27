# Eloquent JavaScript (abridged)

## General Resources
Eloquent JavaScript

http://eloquentjavascript.net/

Basic Training Repo

https://github.com/Jbays/js-basic-training

## Table of Contents
1.  Values, Types, and Operators
2.  Program Structure
3.  Functions                
4.  Objects and Arrays
5.  Ready To Apply / Next Steps
6.  Higher-Order Functions
7.  Extra Credit

## 1. Values, Types, and Operators

[Eloquent JavaScript Ch. 1](http://eloquentjavascript.net/01_values.html)

[Variables](/resources/variables.md)

[Crash Course on Types](/resources/type_crash_course.md)

[Strings and Other Types](https://www.javascript.com/learn/javascript/strings)

[String Methods](/resources/string_methods.md)

### Check For Understanding
#### Types
1. JavaScript has how many different types?
2. List all types.  Simply, describe uses for each type.
3. Declare a variable of each type.

#### Strings
4. What is a string?
5. Define your own unique string.
6. Write code to access the third letter in your string.
7. Use a built-in string method to capitalize your string's every letter.
8. Use a built-in string method to lowercase your string's every letter.

```javascript
let basicTrainingString = "Basic Training";
```

9.  Find the index of the letter "T" in basicTrainingString.

```javascript
basicTrainingString.lastIndexOf('i');
```

10. What does the above code return?
11. Using string.slice, return "Basic".
12. Using string.slice, return "Training".

## 2. Program Structure

[Eloquent JavaScript Ch. 2](http://eloquentjavascript.net/02_program_structure.html)

[Conditionals for Beginners](https://www.w3schools.com/js/js_if_else.asp)

[Conditionals for Beginners pt. 2](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals)

[Conditionals for Intermediates](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)

[Loops for Beginners](https://www.w3schools.com/js/js_loop_for.asp)

[Loops for Beginners pt. 2](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code)

[For-loops for Intermediate](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for)

### Check For Understanding
#### Conditionals
1. Write a conditional
2. Write another conditional.  In plain language, explain your conditional code.
3. Write an if-else conditional.
4. Write an if -- else if -- else conditional.

#### For-Loops
5. Write a for-loop that logs 1 through 100 to the console.
6. Write a for-loop that logs EVEN NUMBERS 1-100 to the console.
7. Write a DECREMENTING for-loop that logs 100 through 1 to the console.

## 3. Functions

[Eloquent JavaScript Ch. 3](http://eloquentjavascript.net/03_functions.html)

[Intro To Functions](/resources/intro_to_func.md)

[Basic Use of Functions](/resources/basics_func.md)

[Defining Functions](/resources/defining_func.md)

[Functions Make Values](/resources/funcs_make_values.md)

### Check For Understanding (Functions I)

#### 1. What is the basic anatomy of a function?

#### 2. Write a function called "basicFunction".

```javascript
basicFunction() //==> "hello world"
```

#### Description
* As input, basicFunction takes nothing.
* As output, basicFunction logs to the console "hello world"
* Write first as a "function expression".
* Write second as a "function declaration".

### NOTE
From now on, write your functions in **function declaration**.

#### 3. Write a function called "sayHello".
```javascript
sayHello('joe')          //==> "hello joe"
sayHello('Tommy')        //==> "hello Tommy"
sayHello('Frankenstein') //==> "hello Frankenstein"
```

#### Description
* As input, sayHello takes a string.
* As output, sayHello logs to the console "hello"+<input>

#### 4. Write a function called "addTwoNums".
```javascript
addTwoNums(2,4)   //==> 6
addTwoNums(7,9)   //==> 16
addTwoNums(12,32) //==> 44
```

#### Description
* As input, addTwoNums takes two numbers.
* As output, addTwoNums returns the result.

#### 4. Write a function called "containsLetter".
```javascript
containsLetter("anna","a")   //==> true
containsLetter("anna","b")   //==> false
containsLetter("anna","n")   //==> true
containsLetter("anna","z")   //==> false
containsLetter("abcdefghij","e") //==> true
containsLetter("abcdefghij","k") //==> false
```

#### Description
* As input, containsLetter takes two strings.
* As output, containsLetter returns a boolean indicating whether the second input is contained in the first.

#### 5. Write a function called "fizzBuzz".
```javascript
fizzBuzz()
//1
//2
//"fizz"
//4
//"buzz"
//"fizz"
//7
//8
//"fizz"
//"buzz"
//11
//"fizz"
//13
//14
//"fizzBuzz"
```

#### Description
* As input, fizzBuzz takes nothing.
* As output, fizzBuzz prints numbers 1 thru 100 to the console.
//**              (1). For multiples of 3, instead print "Fizz"
//**              (2). For multiples of 5, instead print "Buzz"
//**              (3). For multiples of 3 & 5, instead print "FizzBuzz"

## 4. Objects and Arrays

[Eloquent JavaScript Ch. 4](http://eloquentjavascript.net/04_data.html)

[Intro To Arrays](/resources/intro_to_arrays.md)

[Objects for Beginners](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics)

[Object for Beginners pt. 2](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)

### Check For Understanding
#### Arrays I
1. Write an array called "fruits" which contains three different fruits.
2. How can I access the second piece of fruit in fruits array?
3. Use simple array methods to add fruit to the fruits array.
4. Use simple array methods to remove fruit from the fruits array.
5. What means fruits.length?

```javascript
let pizzaTypes = ['deepDish','Neapolitan','thinCrust','bad'];
```

### Check For Understanding
#### Arrays II
1. How to access 'Neapolitan'?  And 'bad'?
2. Add a few elements in pizzaTypes array.  Remove 'thinCrust'.
3. What are the four most common array methods for adding / removing elements?
4. Give code examples of all four.
5. Use the concat method on pizzaTypes.  Note: You will need to create another array.
6. Use join to turn an array into a string.  Use split to turn string into array.
7. Use Math.floor and Math.random to generate random integers.

### Check For Understanding
#### Objects I
1. What's a key-value pair?  Make an object to illustrate.
2. What's the difference between objects and arrays?
3. Create an object using object literal syntax.
4. Add and access values using both bracket and dot notation.
5. Combine objects with arrays.  Combine arrays with objects.

### Check For Understanding
#### Objects II
1. Create an empty object called "pet".
2. To your pet object, add "name", "color", "age", and "isFavorite" key-value pairs.  "name" and "color" type are strings.  "age" is a number.  "isFavorite" is boolean.
3. To "pet" object, use dot notation to add another key-value pair.  You choose specifics.
4. To "pet" object, use bracket notation to add another key-value pair.  You choose specifics.

## 5. Ready To Apply / Next Steps

Interested in applying to Galvanize's Web Development Immersive?

Successful applicants can solve the coding challenge below.

### Coding Challenge
1. Write a function called locateHighestSum

```javascript
let sampleArr = ["111","222","333","999","636363","9792","123"];
locateHighestSum(sampleArr) // ==> 5
```
#### Description
* As input, locateHighestSum should take an array.
* As output, locateHighestSum should find the element with the highest sum.  Then return that element's index.
* In case of ties, return the highest index.


### Extra Credit - Higher-Order Functions

[Eloquent JavaScript Ch. 5](http://eloquentjavascript.net/05_higher_order.html)

[Leveraging Multiple Functions](/resources/multi_functions.md)

[Higher-Order Functions](/resources/adv_array_methods.md)

### Check For Understanding (Functions II)
#### 1. Write a function called "iFindMax"

```javascript
let randomNumbers = [1,6,7,8,11,2,3,9]
iFindMax(randomNumbers) //==> 11
```

#### Description
* For input, iFindMax takes an array.
* For output, iFindMax returns the highest number in the array.

#### 2. Write a function called "iFindMin"

```javascript
let randoNumbos = [1,6,-7,8,11,-2,3,9]
iFindMin(randoNumbos) //==> -7
```
#### Description
* For input, iFindMax takes an array.
* For output, iFindMax returns the lowest number in the array.

#### 3. Write a function called "iLikeToAdd"

```javascript
let randoNumbos = [1,6,-7,8,11,2,3,9]
iLikeToAdd([1,2,3])     //==> 6
iLikeToAdd(randoNumbos) //==> 33
```
#### Description
* For input, iLikeToAdd takes an array.
* For output, iLikeToAdd returns the sum of all array's elements.

### Check For Understanding (Functions III)

#### 1. Write a function called myForEach

```javascript
let oldSchoolMovie = ["Frank", "The", "Tank"]
myForEach(oldSchoolMovie,console.log) //==> "Frank","The","Tank"
```
#### Description
* myForEach takes two parameters.  First is an array.  Second is a callback.
* myForEach should apply the callback to each element in the array.

#### 2. Write a function called myMap

```javascript
let simpleNums = [1,2,3]
myMap(simpleNums,multipleByThree) // ==> [3,6,9]
```
#### Description
* myMap takes two parameters.  First is an array.  Second is a callback.
* myMap applies callback to each element in the input array.
* As output, myMay returns the new array.

#### 3. Write a function called myFilter

```javascript
let simpleNums = [1,2,3,4,5,6]
myForEach(simpleNums,keepOddsOnly) //==> [1,3,5]
```
#### Description
* myFilter takes two parameters.  First is an array.  Second is a callback that returns true or false.
* As output, returns an array of all elements whose callback returned true

### Extra Credit - CodeWars

[CodeWars](http://codewars.com)

[CodeWars Ranking System](https://www.codewars.com/docs)

Studying/Training on CodeWars will help prospective students prepare for Galvanize's admissions.  

Complete five (5) coding challenges of 7 kyu difficulty.  This is challenging.

But the practice helps ensure your smooth transition from mere applicant to Galvanize student.  In other words, this juice is worth the squeeze.
