# JavaScript Starters Syntax Guide

## Variables

Variables are used to store and call/reference data.

```
var newVariable = "I am a variable!"
```


Variables are essential and can be used for a multitude of different things. We will dive more into all of these things as we continue through the guide.

Variables can also be declared with let. The difference between let and var is the scope of the variable. let variables are block scoped, var variables are globally scoped. This means that let variables are only available within where they are defined, and var variables are available throughout the entire code. 

```
let newLetVariable = "I am also a variable!"
```

## Comparison Statements

With comparison statements, we are comparing data to execute functions determined by differences.

```
var x = 3;
x == 3;
```

The above would return true, we can then take true and use it to execute functions.

```
var x = 3;
x == 8;
```

The above would return false, see how this can be used? For example, think about comparing a password, true lets you in, false denies access.

There are a few different types of comparisons, lets take a look at some with the chart below:

| Statment | Use                                                                   |  
|----------|-----------------------------------------------------------------------|
| =        | An assignment operator, NOT a comparison statement (commonly confused)|
| ==       | Equal to                                                              |
| ===      | Equal data type (IE: 5 is a digit, check if digit)                    |
| !=       | Not Equal to                                                          |
| !==      | Not Equal data type                                                   |
| >        | Greater than                                                          |
| <        | Less than                                                             | 
| >=       | Greater than or equal to                                              |
| <=       | Less than or equal to                                                 |

## Boolean Statements

Boolean statements are true and false statements, often used in comparisons or returned from them.

```
x = true;
y = false;
```

Boolean operators are used to get more specific with the return of a statement, see the chart below:

| Operator | Use |
|----------|-----|
| &&       | And |
| \| \|    | Or  |
| !        | Not |

an example of and:

```
var x = 3;
var y = 6;

if(x == 3 && y == 6) {
    z = true;
} else {
    z = false;
};
```

If you said this would return true, you would be correct. "if else" statments are used to return data in a decision making manner. It will execute the "if" code when it matches, when "if" doesn't match, it will execute the "else" code.

## Arrays

Arrays are similar to variables, they store values/data. The difference is that they store more than one piece of data at a time. Arrays can store most values that variables are able to store.

```
const newArray = [1, 7, 25];
```

const stands for constant reference to an array. You can also declare an array with let. You use square brackets to contain your data, and use comas between each piece as separation.

Arrays can also store multiple data types at the same time:

```
let dataParty = ["string value", 8, true]
```

you can call one piece of data from an array if you target it. The ordering of arrays start at 0 rather than one:

```
console.log(dataParty[1])
// 8 will be returned to the console
```

## Objects

Objects are a type of entity that contain a collection of data with multiple properties. They are different from an array as they contain data in seperate variables, rather than all in one.

```
var car = {
    make: "toyota",
    model: "mr2",
    year: 1991,
    color: "yellow"
};
```

Note that there are multiple types of data declared in the object, like arrays you can declare different data types in objects. Use comas to seperate each declaration within the object.

You can target a specific piece of data from an object like so:

```
console.log(car.model);
// mr2 will be returned to the console
```

It is possible to have functions within objects as well, this way if you are creating a function specifically for an object, you can have it all contained inside of an object for better organization. This process is called encapsulating.

```
var car = {
    make: "toyota",
    model: "mr2",
    year: 1991,
    color: "yellow",
    description: function() {
        return "A " + this.make + " " + this.model + " is a great car, my personal favorite is a " + this.color + " " + this.year + " that my dad once owned.";
    }
};

console.log(car.description());
// This would log: "A toyota mr2 is a great car, my personal favorite is a yellow 1991 that my dad once owned." to the console.
```

Here, we first declare a function (functions will be further defined below). Then it is started with return, if return isnt specified the function will not return any value from the object and will be undefined. "this" is used to target properties within this object. Then the function is logged to the console using proper object targeting.


## Functions

Functions are a piece of code that are made to execute an action. Some functions are built into JS, but you can also make your own.

```
function quickMath() {
    let x = 1;
    let y = 1;
    console.log(x + y);
};

quickMath();
```

This is a function that takes two variables defined as 1 and adds them together in the console. The function "quickMath" is called at the bottom, once it is called it will be executed. During its execution, it defines x and y as 1, and then console logs x + y (1 + 1) and displays the result (2) to the console.

Functions are an essential part of JS, we will continue to explore their capabilities below.

## Functions & Parameters

Functions can also have specified parameters that are given to it by arguments.

```
function quickMathEnhanced(p1, p2) {
    console.log(p1 + p2);
};

quickMathEnhanced(1 + 1);
// 1 + 1 are the arguments, p1 and p2 are the parameters.
```

This function will also log 2 to the console, the difference is instead of declaring variables we use arguments to fill parameters.

You can also use functions and parameters to define variables

```
let x = quickMathAscended(5, 5, 5);

function quickMathAscended(p1, p2, p3) {
    return p1 + p2 + p3;
};
```

When the function is called, it will return to x. In this case, 5 + 5 + 5 will be calculated, and 15 will be declared as the value of x.

## Loops

A loop is used to loop through a function and perform an action a multitude of times. This is useful when you need actions to be performed multiple times, for example, you need a function to execute for every piece of data stored in an array.

there are multiple types of loops, let's start with a while loop. A while loop executes its function until the specified parameter is no longer true.

```
let i = 0;

while (i < 20) {
    console.log("hello world!");
    i++;
};
```

An easy way to understand this is by writing it out, this loop says "While i is less than 20, log "hello world!" to the console, then increase i by 1". Since i is originally declared as 0, this loop will log "hello world!" to the console 20 times.

Let's have a look at another type of loop, for loops. For loops are similar to while loops, but their parameters are different. A variable is declared within them, and so is the incremental increase of said variable.

```
fruits = ["apples", "oranges", "bananas"];

for (i = 0; i < fruits.length; i++) {
    console.log("I love " + fruits[i]);
};
```

First, an array called fruits is declared and defined with 3 elements. Then we execute a for loop that says "i = 0, if i is less than the length of the fruits array, execute this loop and increase i by 1. Then it is logged, and i is indicated as the element number called from the array. It starts and 0 (apples), then increases to 1 (oranges), then 2 (bananas). The final result of this loop shows "I love apples" "I love oranges" "I love bananas" logged to the console.

## Data Types

Data types are used for declaring different kinds of values, some of the most common data types are:

- Strings: A string of text. example: "string"
- Integers: A number. example: 7
- Characters: A single character. example: "P"
- Booleans: True and False.
- Nulls: Represents no value.
- Undefined: A variable that is declared but has no value defined.

## Comments

Comments are very useful, they are like notes. Comments don't change the code at all, but they allow you to add descriptions of what code does and communicate with other programmers working on the same code. You saw a few of them throughout this guide. Here is another example:

```
// This is a comment
```