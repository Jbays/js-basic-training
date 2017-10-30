//(This class will teach an abridged version of Eloquent Javascript)

//If you can complete this worksheet, we want to talk to you.
//You might be ready to apply

//=============================================
//       Table of Contents        | line number
//=============================================
//0. Resources                    | 19-28
//1. Values, Types, and Operators | 32-57
//2. Program Structure            | 61-76
//4. Objects and Arrays           | 80-120
//3. Functions                    | 122-166
//5. Higher-Order Functions       | 170-268
//6. Ready To Apply / Next Steps  | 272-286
//=============================================

/////////////////////////////////////////
//0. RESOURCES - RESOURCES - RESOURCES
//
// 1. Eloquent Javascript
// http://eloquentjavascript.net/
//
// 2. Galvanize Basic Training Repo
// https://github.com/gSchool/js-basic-training/
//
// 3. CodeWars - Beat 5 Level-7 challenges
// https://www.codewars.com/
/////////////////////////////////////////

/////////////////////////////
//1. Values, Types, Operators

//1.1. Learn about types in Javascript
//https://github.com/gSchool/js-basic-training/blob/dev/markdown/type_crash_course.md

//QUESTIONS - QUESTIONS - QUESTIONS
//(a) JavaScript has how many different types?
//(b) Please list all types
//(c) Please declare a variable of each type.

//1.2. Learn About Strings
//https://github.com/gSchool/js-basic-training/blob/dev/markdown/string_methods.md
//(a) What is a string?
//(b) Define your own string.
//(c) Access the third letter in your string.
//(d) Use a built-in string method to capitalize your string's every letter.
//(e) Use a built-in string method to lowercase your string's every letter.

//Given this code:
//NOTE: let basicTrainingString = "Basic Training";
//(f) Write code which'll find the index of the letter "T" in basicTrainingString.
//(g) What will this code return?
//    (1) basicTrainingString.lastIndexOf('i');
//(h) Using string.substring
//    (1) Write code which will return "Basic".
//    (2) Write code which will return "Training".
/////////////////////////////

///////////////////////
//2. Program Structure

//2.1. Conditionals
//QUESTIONS - QUESTIONS - QUESTIONS
//(a) Write a conditional
//(b) Write another conditional.  In plain language, explain what your conditional does.
//(c) Write an if-else conditional.
//(d) Write an if-(else-if)-else conditional.

//2.2. For-loop
//QUESTIONS - QUESTIONS - QUESTIONS
//(a) Write a for-loop that logs 1 through 100 to the console.
//(b) Write a for-loop that logs EVEN NUMBERS 1-100 to the console.
//(c) Write a for-loop that logs 100 thru 1 to the console.
///////////////////////

/////////////////////////////////////
//4. Data Structures: Objects and Arrays
//4.1. Learn about Arrays
// https://github.com/gSchool/js-basic-training/blob/dev/markdown/intro_to_arrays.md

//QUESTIONS - QUESTIONS - QUESTIONS
//(a) Write an array called "fruits" which contains three different fruits.
//(b) How can I access the second piece of fruit in fruits array?
//(c) Use simple array methods to add fruit to the fruits array.
//(d) Use simple array methods to remove fruit from the fruits array.
//(e) What means fruits.length?

//4.2. Learn about Objects
//https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics

//QUESTIONS - QUESTIONS - QUESTIONS
//(a) Create an empty object called "pet".
//(b) To your pet object, add "name", "color", "age", and "isFavorite" key-value pairs.
//NOTE: type for "name" and "color" are string.
//      type for age is number.
//      type for isFavorite is boolean.
//(c) To "pet" object, use dot notation to add another key-value pair.  You choose specifics.
//(d) To "pet" object, use bracket notation to add another key-value pair.  You choose specifics.

//4.3. Arrays II
//QUESTIONS - QUESTIONS - QUESTIONS
//NOTE: let pizzaTypes = ['deepDish','neopolitan','thinCrust','bad'];
//(a) How to access 'neopolitan'?  And 'bad'?
//(b) Add a few elements in pizzaTypes array.  Remove 'thinCrust'.
//(c) What are the four most common array methods for adding / removing elements?
//(d) Give code examples of all four.
//(e) Use the concat method on pizzaTypes.  Note: You will need to create another array.
//(f) Use join to turn an array into a string.  Use split to turn string into array.
//(g) Use Math.floor and Math.random to generate random integers.

//4.4. Objects II
//QUESTIONS - QUESTIONS - QUESTIONS
//(a) What's a key-value pair?  Make an object to illustrate.
//(b) What's the difference between objects and arrays?
//(c) Create an object using object literal syntax.
//(d) Add and access values using both bracket and dot notation.
//(e) Combine objects with arrays.  Combine arrays with objects.
/////////////////////////////////////

///////////////
//3. Functions

//3.1. Intro to Functions
//https://github.com/gSchool/js-basic-training/blob/dev/markdown/intro_to_javascript_functions.md

//3.2. Basic Use of Function
//https://github.com/gSchool/js-basic-training/blob/dev/markdown/basic_use_of_functions.md

//3.3. Defining Functions
//https://github.com/gSchool/js-basic-training/blob/dev/markdown/defining_functions.md

//QUESTIONS - QUESTIONS - QUESTIONS
//(a) What is the basic anatomy of a function?
//(b) In two different styles, write a basic function called "basicFunction".
//    NOTE: Your function should log inputs to the console.
//    (1) First time use "function definition".
//    (2) Second time use "function expression".

//NOTE: From now on, write your functions in the "function definition" style.
//(c) Define your own function called "numberUpToLogger".
//    (1) For input, your function should take a number.
//    (2) For output, starting at zero your function should log every number up to & including the input number.
//    NOTE: SAMPLE OUTPUTS
//    numberUpToLogger(5) ==> //1,2,3,4,5
//    numberUpToLogger(10) ==> //1,2,3,4,5,6,7,8,9,10

//(d) Define a new function called "numbersUnder100"
//    (1) For input, your function should take a string.
//    (2) For output, your function should return every number between input string && 100.
//    NOTE: SAMPLE OUTPUTS
//    numbersUnder100(97) ==> //97,98,99
//    numbersUnder100(90) ==> //90,91,92,93,94,95,96,97,98,99
//    numbersUnder100(1)  ==> //1,2,3,...,97,98,99

//(e) What's the difference between a function using console.log and return?
//    (1) Should every function have a return statement?
//    (2) Should every function have a console.log?

//(f) Will this function successfully log to the console?  Why or why not?
//    NOTE:
//      function logToConsole(){
//       return;
//       console.log("Talking To The Console!");
//      }
//      logToConsole();
///////////////

///////////////////////////
//5. Higher-Order Functions

//5.1. Functions That Make Values
//https://github.com/gSchool/js-basic-training/blob/dev/markdown/functions_that_make_values.md

//5.2. Passing Functions As Arguments
//https://github.com/gSchool/js-basic-training/blob/dev/markdown/leveraging_multiple_functions.md

//5.3. Leveraging Multiple Functions
//https://github.com/gSchool/js-basic-training/blob/dev/markdown/leveraging_multiple_functions.md

//NOTE: From now on, write your functions in the "function definition" style.
//QUESTIONS - QUESTIONS - QUESTIONS
//(a) Write a function called "iFindMax".
//    (1) For input, iFindMax takes an array
//    (2) For output, iFindMax returns the highest number in the array parameter
//    NOTE: let randomNumbers = [1,6,7,8,11,2,3,9]
//    NOTE: SAMPLE OUTPUTS
//    iFindMax(randomNumbers) ==> 11

//(b) Write a function called "iFindMin".
//    (1) For input, iFindMax takes an array
//    (2) For output, iFindMax returns the lowest number in the array parameter
//    NOTE: let randoNumbos = [1,6,-7,8,11,-2,3,9]
//    NOTE: SAMPLE OUTPUTS
//    iFindMin(randoNumbos) ==> -7

//(c) Write a function called "iLikeToAdd"
//    (1) iLikeToAdd takes two parameters.
//    (2) As output, iLikeToAdd returns the sum of both parameters
//    NOTE: let randoNumbos = [1,6,-7,8,11,-2,3,9]
//    NOTE: SAMPLE OUTPUTS
//    iLikeToAdd(7,4)   ==> 11
//    iLikeToAdd(13,-4) ==> 9

//(d) Write a function called "printCatFaces"
//    (1) As input, printCatFaces takes a number
//    (2) As output, printCatFaces prints an array full of catFaces.
//    NOTE: array.length should equal input number
//    NOTE: let catFace = "(^-人-^)"
//    NOTE: SAMPLE OUTPUTS
//    printCatFaces(2) ==> ["(^-人-^)","(^-人-^)"]
//    printCatFaces(4) ==> ["(^-人-^)","(^-人-^)","(^-人-^)","(^-人-^)"]
//    (3) Change printCatFaces output to be a SINGLE string.
//    printCatFaces(2) ==> "(^-人-^)(^-人-^)"
//    printCatFaces(4) ==> "(^-人-^)(^-人-^)(^-人-^)(^-人-^)"

//(e) Write a function called "returnShortest"
//    (1) As input, returnShortest takes a string.
//    (2) As output, returnShortest returns length of the shortest word contained inside input string.
//    NOTE: let theDoorsLyrics = "had shoulders smooth as ravens claws"
//    NOTE: SAMPLE OUTPUTS
//    returnShortes(theDoorsLyrics) ==> 2

//(f) Write a function called sumArrayOfArrays which will return the sum of ALL nestedArrays.
//    NOTE: let arrayOfArrays = [[3,4,6,8,1],[3,6,7,9,0],[5,6,4,3,8]]

//(g) Write two functions.  takeActions and sirYesSir.
//    NOTE: sirYesSir must be called INSIDE takeActions
//    takeActions
//    (1) As input, takeActions takes a string.
//    ex. ==> "mow the grass", "shine shoes"
//    (2) As output, takeActions returns string "Sir, I [inputString], sir!"
//    ex. takeAction('mowed the grass') ==> "Sir, I mowed the grass, sir!"
//    sirYesSir
//    (1) As input, sirYesSir takes a string.
//    (2) As output, sirYesSir appends text then returns new string:
//        (i).  Prepend "Sir" to the string's beginning.
//        (ii). Append ", sir!" to the string's end

//5.4. Higher-Order Array Methods
//https://github.com/gSchool/js-basic-training/blob/dev/markdown/higher_order_array_methods.md

//(h) Write a function called myForEach.
//    (1) myForEach takes two parameters.  First is an array.  Second is a callback.
//    myForEach should apply the callback to each element in the array param.
//    NOTE: let oldSchoolMovie = ["Frank", "The", "Tank"]
//    NOTE: SAMPLE OUTPUTS
//    myForEach(oldSchoolMovie,console.log) ==> "Frank","The","Tank"

//(i) Write a function called myMap
//    (1) myMap takes two parameters.  First is an array.  Second is a callback.
//    (2) myMap applies callback to each element in the input array.
//    (3) As output, myMay returns the new array.
//    NOTE: let simpleNums = [1,2,3]
//    NOTE: SAMPLE OUTPUTS
//    myMap(simpleNums,multipleByThree) ==> [3,6,9]

//(j) Write a function called myFilter
//    (1) myFilter takes two parameters.  First is an array.  Second is a callback that returns true or false.
//    (2) As output, returns an array of all elements whose callback returned true
//    NOTE: let simpleNums = [1,2,3,4,5,6]
//    NOTE: SAMPLE OUTPUTS
//    myForEach(simpleNums,keepOddsOnly) ==> [1,3,5]

//5.5 CodeWars
//(a) Sign up for CodeWars.  Beat 5 Level-7 challenges.
//    NOTE: Below is an example problem
//    https://www.codewars.com/kata/sum-and-multiply
///////////////////////////

///////////////////////////////////////////////////
//6. Ready To Apply / Next Steps Challenge Question

//Are you ready to take Galvanize's takehome exam?

//BOSS FIGHT! - BOSS FIGHT! - BOSS FIGHT!

// FINAL
//given the following array:
//let sampleArr = ["111","222","333","999","636363","9792","123"];
//write a function called findHighestSum
//findHighestSum should take an array as its input
//As output, findHighestSum should return the index of the element w/the greatest sum.
//In case of ties, return the highest index.

//findHighestSum(sampleArr) should return
///////////////////////////////////////////////////
