# JavaScript Basics

## Building blocks of (almost) every programming language


## How this looks like in JavaScript
### Comments on Styles
In these examples, I'll use names written between hashtags, in caps lock, to denote placeholders. Like this: #PLACEHOLDER#, or this: #PLACE_HOLDER#.

### Comments on tools we use
Often times when looking at examples, it helps to use code that does something visible. One of the easiest ways of doing that in JavaScript is the __console.log__ function, which takes almost anything as a parameter and just writes it to the debug console.

### Variables
There are three ways of defining variables in JavaScript. The syntax for these is mostly the same, and we'll go them through one by one.

#### var
Historically, var was the only option we had, and so we will start with it. The Syntax is:
```
  var #VARIABLE_NAME# = #INITIAL_VALUE#;
```

An example would be:
```
  var princessName = 'Veronica';
```
In this example the name of the variable is __princessName__ und the initial value is 'Veronica'.

__Var__ describes a variable, but it is not clear, if this variable is a constant or the variable can be re-assigned.

#### const
To specify if a variable is a constant, one now uses the term __const__  .

##### What is a constant?
A constant is a fixed and well-defined value and it will not change.

To denote that the constant is a physical one and we can assume that its value is of common knowledge, we write the name in CAPITAL_NOTATION.
An example for a physical constant is the pi, which was defined once and is now more or less fixed:
```
  const CIRCLE_RATIO = 3.14159265359; // Fixed value for the constant pi.
 ```
If the variable is fixed, but it is not of common knowledge, we use the same notation as for a variable. An example would be, that we look at a dragon, which is the friend of our princess 'Veronica' and this dragon has a defined span of it wings, as it is a grown up, meaning that it won't grow anymore. We can now assign the value for this length:
```
  const dragonWingspan = 24.5; // This is the length between the two edges of the wings of our dragon friend.
```
Therefore the length of the span of the wings of our dragon friend is now 24.5.
Note, that the name of the constant is __dragonWingspan__ and not DRAGON_WINGSPAN, as this value is not of common knowledge.

#### let
For variables which are not a constant, but can change or be re- assigned, the term used is __let__ .

To come back to our above mentioned example, we can specify, that our __var princessName__ is a __let__ , as princesses don't live forever, they might get married and become queens, they might die or become sisters that are also princesses. Therefore this variable can change.
To use the newly learned syntax, we can now define the variable __princessName__ as:
```
  let princessName = 'Veronica'; // 'Veronica' is the current princess.
```
Let's assume, that our current princess now flies of with her dragon friend, meets a beautiful prince that will soon become a king and she marries. Now our princess is a queen and she gives birth to a daugther, which she calles 'Isabell'.
How does these changes apply to our example?
We can now define a new variable for the current name of the queen, which is our former princess:
```
  let queenName = princessName; // This returns 'Veronica' and assigns it to the new variable queenName.

```
We can also update the variable __princessName__ , as we now have a new princess, called 'Isabell':
```
  princessName = 'Isabell'; // The name of the current princess is now 'Isabell', not 'Veronica' anymore.
```

### Arrays
Often times when writing code, we will encouter situations that call for lists of items, in one form or another. Think of these examples:

* The name of all friends of a user for a social media platform.
* The items you have selected for purchase in an online shop.
* The highest scores you have ever achieved in Tetris.

While writing software, you will encounter lists such as these almost constantly. In JavaScript, a common way of representing such data structures is with __arrays__.

Let's first look at how we use them, before we discuss their properties.

#### Defining an array
Arrays in JavaScript are a type of value. This value is represent by comma seperated __items__ that are placed inside of square brackets. The following code defines a new constant with the name of numberArray, that is assigned a list with the items 1, 5 and 8.

```javascript
  const numberArray = [1, 5, 8];
```

Let's do something similar for string values. The following code defines a new changeable variable with named "friendList" with four names as items.

```javascript
  let friendList = ['Maria', 'Frank', 'Tim', 'Anna'];
```

#### Accessing items on an array
Array items can be accessed by their numeric index, where the first item has the index 0 and subsequent items have the indexes 1, 2, 3 and so on. Accessing over indexes can be done for retrieving values from an array, for overwriting existing items, and also for creating new indexes.

In the following code, we'll create a new array of prime numbers, and log it's first item (the item with the index 0) to the console.

```javascript
  const primeNumberArray = [2, 3, 5, 7];
  console.log(primeNumberArray[0]);
```
