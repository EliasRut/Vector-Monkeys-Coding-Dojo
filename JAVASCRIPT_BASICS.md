# JavaScript Basics

## Building blocks of (almost) every programming language


## How this looks like in JavaScript
### Comments on Styles
In these examples, I'll use names written between hashtags, in caps lock, to denote placeholders. Like this: #PLACEHOLDER#, or this: #PLACE_HOLDER#.

### Comments on tools we use
Often times when looking at examples, it helps to use code that does produces a visible effect. One of the easiest ways of doing that in JavaScript is the __console.log__ function, which takes almost anything as a parameter and just writes it to the debug console. The following code logs the text 'Welcome to the Vector Monkeys Coding Dojo!' to the developer console.

```javascript
  console.log('Welcome to the Vector Monkeys Coding Dojo!');
```

### Variables
There are three ways of defining variables in JavaScript. The syntax for these is mostly the same, and we'll go them through one by one.

#### var
Historically, var was the only option we had, and so we will start with it. The Syntax is:

```javascript
  var #VARIABLE_NAME# = #INITIAL_VALUE#;
```

In the following example, we create a new variable with the name __princessName__ and an initial value of 'Veronica'.

```javascript
  var princessName = 'Veronica';
```

The drawback of using __var__ is it's ambiguity: it is not clear if this variable is a constant, or if the variable can be re-assigned. This can make the intention of the programmer that has written the code harder to understand. Therefore, we will always use the modern way of specifying variables: using __const__ and __let__.

#### Variable naming
JavaScript uses so called __camelCase__ for most variable naming. This is a not a requirement of the language, but rather a best practice that most developers agree to. Camel case consists of:
* a small, non numeric letter as the first character of the name
* a capital letter on word boundaries, for example princessName
* only english letters, as well as numbers 0-9
* no other characters, specifically no white spaces, slashes, dashes, dots, commas etc.

#### const
To specify if a variable is a constant, one now uses the term __const__.

A constant is a variable with a fixed, unchangable value, so a value that __can not be changed__ in a later part of the programm.

Sometimes, we want to denote that a constant is not defined due to how we have written and intened the code to be, but rather a "real" constant, such as a physical or mathematical one. For such cases, it is common practice to use CAPITAL_NOTATION. An example for a physical constant is the pi, should we need to include it to some decimal point in our code, we could do the following:

```javascript
  const CIRCLE_RATIO = 3.14159265359; // Fixed value for the constant pi.
 ```

For all other cases, we use the same notation as we do for any other variable. An example would be that we look at a dragon, a good friend of our princess 'Veronica', and definy that this dragon has a fixed wingspan since it is all grown up. The following code would assign a constant dragonWingspan with an imaginary value for it:

```javascript
  const dragonWingspan = 24.5; // This is the length between the two edges of the wings of our dragon friend.
```
Therefore we have now defined the length of the span of the wings of our dragon friend to be 24.5.

#### let
For variables which are not a constant, but can change or be re- assigned, the keyword to be used is __let__ .

To come back to our above mentioned example, we can specify, that our __var princessName__ is a __let__ , as princesses don't live forever, they might get married and become queens, they might die or become sisters that are also princesses. Therefore this variable can change.
To use the newly learned syntax, we can now define the variable __princessName__ as:

```javascript
  let princessName = 'Veronica'; // 'Veronica' is the current princess.
```
Let's assume, that our current princess now flies of with her dragon friend, meets a beautiful prince that will soon become a king and she marries.
Now our princess is a queen and she gives birth to a daugther, which she calles 'Isabell'.

How would these changes apply to our example?
We can now define a new variable for the current name of the queen, which is our former princess:

```javascript
  let queenName = princessName; // This returns 'Veronica' and assigns it to the new variable queenName.
```

We can also update the variable __princessName__ , as we now have a new princess, called 'Isabell':

```javascript
  princessName = 'Isabell'; // The name of the current princess is now 'Isabell', not 'Veronica' anymore.
```

### Arrays
Often times when writing code, we will encounter situations that call for lists of items, in one form or another. Think of these examples:

* The name of all friends of a user for a social media platform.
* The items you have selected for purchase in an online shop.
* The highest scores you have ever achieved in Tetris.

While writing software, you will encounter lists such as these almost constantly. In JavaScript, a common way of representing such data structures is with __arrays__.

Let's first look at how we use them, before we discuss their properties.

#### Defining an array
Arrays in JavaScript are a type of value. This value is represent by comma seperated __items__ that are placed inside of __square brackets []__. The following code defines a new constant with the name of numberArray, that is assigned a list with the items 1, 5 and 8.

```javascript
  const numberArray = [1, 5, 8];
```

Let's do something similar for string values. The following code defines a new changeable variable with named "friendList" with four names as items.

```javascript
  let friendList = ['Maria', 'Frank', 'Tim', 'Anna'];
```

#### Accessing items on an array
Array items can be accessed by their numeric index, where the first item has the index 0 and subsequent items have the indexes 1, 2, 3 and so on. Access over indexes can be done for retrieving values from an array, for overwriting existing items, and also for storing new items on the array.

In the following code, we'll create a new array of prime numbers, and log it's first item (the item with the index 0) to the console.

```javascript
  const primeNumberArray = [2, 3, 5, 7];
  console.log(primeNumberArray[0]);
```
