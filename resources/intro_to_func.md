# Introduction to JavaScript Functions

Functions are pieces of code that **do** things. JavaScript programs are collections of functions, each function being a smaller program unto itself. The ability to use built-in JavaScript functions, to build our own functions for use, and to organize our code into concise and well-organized functions, is one of the very most central skills to becoming an effective JavaScript programmer.

This sections introduces functions at a *high level*, meaning, we will be focusing on some of the main concepts surrounding functions, and not, the specifics of using them. In the next section we will turn to the specifics of using functions.

## Objectives

By the time you complete this section you should be able to explain to someone else that:

- Functions **do** things and can therefore be thought of as **verbs**
- Functions can also **make** things
- Functions can also be given things that affect what they do
- Functions can be reused

## Functions are Verbs

**Functions _do_ things, and should therefore be thought of as the _verbs_ of your program.**

Consider the following JavaScript code, which runs a series of functions. Don't worry if some of the syntax is unfamiliar at this time:

```javascript
wakeUp();
brewCoffee();
drinkCoffee();
eatBreakfast();
cleanUp();
goToWork();
```

This program **does** several things, and is using several functions to **do** these things. Because the programmer who wrote the code above chose to name their functions as verbs, it makes for a clear and easy to read program.

## Some Functions Make Something

**While every function _does_ something, some functions also _make_ something.**

In our lives as well sometimes when we *do* something, we also *make* something:

- When we **do** the activity of brewing coffee we **make** coffee
- When we **do** the activity of going to work we **make** money

Compare this to things we might do where we do **not make** something:

- When we wake up we **do** something but we **do not make** something new (philosophical discussions aside)
- When we drink coffee we **do** something but we **do not make** something new

With this in mind, here's our example program again, but this time, two of the functions *make* something. Again, don't worry about the specific JavaScript language syntax in this program yet, we will be talking about it at great length later. For now we are just clarifying the mental models that will allow us to write code effectively:

```javascript
wakeUp();

let coffee = brewCoffee(); // The act of brewing coffee makes something new: coffee

drinkCoffee();
eatBreakfast();
cleanUp();

let money = goToWork();    // The act of going to work results in a new thing: money
```

## Some Functions Can Be Given Things to do Work With

Some of the activities that we do from day to day are very similar, except perhaps for an important detail or two. In cases like this it is perfectly natural to say that we are doing the same thing, only that we are doing it with a different thing, or object or item. For example, I drink several times a day and the activity of drinking is pretty much the same. Sometimes during the day however, I drink water, at other times coffee, or tea, or beer.

Similarly, it can be exceptionally helpful to use functions that while always doing the same action, can do so with a different thing. Here again is our example program, but this time instead of using a `drinkCoffee` function we are using a more general `drink` function, which we could use to drink anything. In this case will use it to drink the coffee that was made by the `brewCoffee` function. Again, the details of the syntax we will be covering extensively in just a bit, for now just aim to grasp that we are able to give something specific to a function that does a general action:

```javascript
wakeUp();
let coffee = brewCoffee();

drink(coffee); // Here we do the activity of drinking with the coffee we just made

eatBreakfast();
cleanUp();
let money = goToWork();
```

Writing generalized functions that can perform their actions on items that we give them is really helpful because it allows us to reuse our functions in a variety of situations. In general, programmers try to avoid writing code that they, or someone else, has already written.

Here's our example again, this time reusing our `drink` function in a number of different ways, and also, doing something with the `money` we made in order to make something else we can use:

```javascript
wakeUp();
let coffee = brewCoffee();
drink(coffee);

eatBreakfast();
cleanUp();

let money = goToWork();
let beer = buyBeer(money) // Here we use the money we made earlier to "make" some beer for our program

drink(beer);              // Here we use the drink function again, but this time with the beer we got
```

## Summary

Functions **do** actions and can be thought of as the verbs that make up our programs. Often times, in addition to doing actions, functions can **make** things. Functions can be given things to affect how they act, and can be reused.

Before proceeding you should be comfortable with the ideas that:

- Functions **do** things and can therefore be thought of as **verbs**
- Functions can also **make** things
- Functions can also be given things that affect what they do
- Functions can be reused

## Self Assessment

:question: Which of the following functions appear to be **making** something?

```javascript
wait();
think();
let code = writeCode();
```

:question: Which of the following functions are being **given something** to affect how it runs?

```javascript
grow();
talkTo(friends);
workOnTasks('hack', 'read', 'cook', 'exercise');
sleep();
```

:question: Which of the following functions are being reused?

```javascript
wakeUp();
let coffee = brewCoffee();
drink(coffee);

eatBreakfast();
cleanUp();

let money = goToWork();
let beer = buyBeer(money) // Here we use the money we made earlier to "make" some beer for our program

drink(beer);              // Here we use the drink function again, but this time with the beer we got
```

## Next Steps

Now that you have a high level understanding that functions are the verbs of our programs, it's time to start looking at the specifics of how to use them.
