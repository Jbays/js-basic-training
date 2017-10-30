# Basic Use of Functions

Utilizing functions involves two steps:

1) Defining the function
2) Using the function

A function **must** be defined before it can be used. However, in addition to writing our own function definitions to use (which will covered later), we can also use functions that have already been defined for us. This section will serve as an introduction to using functions by way of using some functions that have already been defined for us anywhere we might choose to write JavaScript code.

## Objectives

By the time you complete this section you should be able to:

- Speak accurately about **calling** and **invoking** functions
- Speak accurately about **passing** functions **arguments**
- Be able to **call** a function and pass it **arguments**

## Terminology for Using Functions

Up until this point in time we have talked about "using" functions, but in fact as programmers we tend to avoid using this ambiguous term. Rather, when we want to "use" a function we say one of the following, which are in fact synonymous:

- That we **call** the function
- That we **invoke** the function

Thus the following statements are all true about the next block of code:

```javascript
eat();
drink();
```

- We are **calling** the `eat` function and then **calling** `drink`
- We are **invoking** `eat` and then **invoking** `drink`
- Here we see the `eat` function being **invoked** before **calling** `drink`
- Here we see 2 function **invocations**, one to `eat` and one to `drink`

> It is worth noting that each of these function calls end with a semicolon `;`. You can think of semicolons in JavaScript as the equivalent to periods in English: they are intended to signify the end of "a sentence". These semicolons are in fact optional, and there are some rather obscure reasons why you might or might not choose to use them which frankly aren't really worth getting into. Rather than describe all the specifics of how to use them, we will include them throughout our code here and you will learn via immersion when and how to use them in your own code, which you should do until a much later period of time when you understand the implications of not using them.

:speak_no_evil: Using **call**, **function**, and **invoke**, read the following lines of code out loud:

```javascript
listen();
read();
practice();
```

Previously we have talked about "giving functions things to affect their behavior", but the actual term for the "thing we give" a function is an **argument**, which we **pass** to a function.

Thus the following statements are all true about the next block of code. Fluency with the technical jargon often results in leaving out some of the terms altogether:

```javascript
drink(coffee);
drink(tea);
cleanUp();
```

- On the first line we call the `drink` function, **passing** `coffee` to it as its only **argument**
- When we call `cleanUp` we do not **pass** it any **arguments**
- First we call `drink` with the `coffee` **argument**, and then with `tea`
- Here we call `drink` with `coffee` and then with `tea`
- We are not calling `cleanUp` with anything

:speak_no_evil: Using **call**, **function**, **invoke**, **pass**, and **argument** read the following lines of code out loud:

```javascript
listen(friend);
read(linesOfCode);
practice(communicating, coding);
```

## Calling Already Defined Functions

**In order to call a function (assuming it has been defined), add opening and closing parenthesis `()` to its name or definition (more on definitions later). If you wish to pass in any arguments, put them inside the parenthesis, separating them by a comma `,` if there are more than one.**

We have already seen this a number of times, but now you have a formal definition.

To explore this we will call some functions that are already defined for us any place where me might run JavaScript code. These functions are called **built in** functions, of which there are many.

The first built in function we will explore is called `console.log`, which takes any number of arguments, and prints them all to the developer console, separated by a space. Here we will call `console.log`, passing it a single argument, the number `1`:

```javascript
console.log(1); // Calling this will result in `1` being logged to the developer console
```

If we pass in more than one argument, `console.log` will print them all to the console separated by a space:

```javascript
console.log(1, 2, 3); // Calling this will result in `1 2 3` being logged to the developer console
```

Admittedly, passing numbers into `console.log` is not going to take us very far, but before we can go into more interesting territory, we need to learn more about what it means to pass in something that we consider a *number*.

## Conclusion

Assuming a function has been defined, either by us or other programmers, we can **call** it and perhaps even **pass** in **arguments** to affect its behavior.

Before moving on to the next section make sure that you can:

- Speak accurately about **calling** and **invoking** functions
- Speak accurately about **passing** functions **arguments**
- Be able to **call** a function and pass it **arguments**

## Self Assessment

:star: In a text editor, call `console.log` by passing it exactly 3 numerical arguments.

## Next Steps

In order to use functions in more ways than simply passing in a number, we now move to a discussion of JavaScript types with a [Crash Course in JavaScript Types](type_crash_course.md), after which we will return to more on the topic of calling functions.

## Table of Contents

### Basic Training Materials

- [Introduction](../README.md)
- [JavaScript and Modern Web Development](modern_web_development.md)
- [Dev Environment Setup](setup.md)
- [Introduction to Functions](intro_to_javascript_functions.md)
- *Basic Use of Functions*
- [JavaScript Types Crash Course](type_crash_course.md)
- [Functions that Make Values](functions_that_make_values.md)
- [JavaScript Types Crash Course](type_crash_course.md)
- [Variables](variables.md)
- [String Methods](string_methods.md)
- [Introduction to Arrays](intro_to_arrays.md)
- [Defining Functions](defining_functions.md)
- [Leveraging Multiple Functions](leveraging_multiple_functions.md)
- [Next Steps](next_steps.md)

### Advanced Content

- [Passing Functions as Arguments](passing_functions_as_arguments.md)
- [Higher Order Array Methods](higher_order_array_methods.md)

### Appendix

- [Reference and Further Study](reference.md)
