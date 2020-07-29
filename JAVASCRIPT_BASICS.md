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




