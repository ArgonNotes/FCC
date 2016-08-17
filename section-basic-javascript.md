# Basic JavaScript
## JavaScript quirky quirks
1. Comments
```javascript
// This is an in-line comment.

/* This is a 
   multi-line comment */
```
2. Data types
	* undefined
	* null
	* boolean
	* string (literal)
	* symbol
	* number
	* object

3. Variables
	* declaration: (with initial value of **undefined**)
	```javascript
	var myName;
	```
	* store value
	```
	myVar = 5;
	myNum = myVar;
	```
	* initialize when declaring
	```
	var newOne = "value assigned at the same time";
	```
	* caseSensitive, cameCase standard
		
4. Math
```
myVar = 5 + 10; // assigned 15
myVar = 12 - 6; // assigned 6
myVar = 13 * 13; // assigned 169
myVar = 16 / 2; // assigned 8

increment number:
i = i + 1;
i++;
decrement 
i--;
```
Decimal numbers are sometimes referred to as floating point numbers or floats.
```
var numDecimal = 5.6;
```
In JavaScript, you can also perform calculations with decimal numbers, just like whole numbers.

Remainder
```
5 % 2 = 1 because
Math.floor(5 / 2) = 2 (Quotient)
2 * 2 = 4
5 - 4 = 1 (Remainder)
+++++++++++++++++++++
17 % 2 = 1 (17 is Odd)
48 % 2 = 0 (48 is Even)
```

Augmented addition, substraction, multiplication, division :
```
myVar += 5;
myVar -= 5;
myVar *= 5;
myVar /= 5;
```
5. Escaping Literal Quotes in Strings
```
var sampleStr = "Alan said, \"Peter is learning JavaScript\".";
var sampleStr = "Alan said, 'Peter is learning JavaScript'.";
var sampleStr = 'Alan said, "Peter is learning JavaScript".';
```
6. Escape Sequences in Strings
```
Code	Output
\'		single quote
\"		double quote
\\		backslash
\n		newline
\r		carriage return
\t		tab
\b		backspace
\f		form feed
```
7. Concatenating Strings
	* plus operator `var ourStr = "Hello, our name is " + "Sylwia.";`
	* plus equals operator `ourStr += "I come second.";`	
	* with variables `var ourStr = "Hello, our name is " + ourName + ", how are you?";`
	* with variables and plus equals operator `ourStr += anAdjective;`

8. String length - found by property `.length`
```
var firstNameLength = 0;
var firstName = "Ada";

firstNameLength = firstName.length;
```
9. Find characters in strings - zero-based indexing
	* `var firstName = "Charles";` 
	* **Bracket notation** `firstName[0];`
	* bracket notation for last character `firstName[firstName.length - 1];`
	* other from the back - `firstName[firstName.length - 3];`
10. Strings in JavaScript are **immutable**.

## Arrays (are mutable)
```
var sandwich = ["peanut butter", "jelly", "bread"].
```

1. Array nesting - **Multi-Dimensional Array**
```
var ourArray = [["the universe", 42], ["everything", 101010]];
```
2. Access data - zero-based indexing
```
var array = [1,2,3];
array[0]; // equals 1
ar data = array[1];  // equals 2
```

* multi-dimensional access

```
var arr = [
    [1,2,3],
    [4,5,6],
    [7,8,9],
    [[10,11,12], 13, 14]
];
arr[3]; // equals [[10,11,12], 13, 14]
arr[3][0]; // equals [10,11,12]
arr[3][0][1]; // equals 11
```

3. **Modify** array with indexes
```
var ourArray = [3,2,1];
ourArray[0] = 1; // equals [1,2,1]
```
### Array manipulation methods

1. `.push()` - takes one or more parameters and "pushes" them onto the end of the array.
2. `.pop()` - is used to "pop" a value off of the end of an array. We can store this "popped off" value by assigning it to a variable.
3. `.shift()` -  it works just like .pop(), except it removes the first element instead of the last.
4. `.unshift()` - works exactly like .push(), but instead of adding the element at the end of the array, unshift() adds the element at the beginning of the array.


## FUNCTIONS
### Function declaration
```
function functionName() {
  console.log("Hello World");
}
```

### Function invoked 
```
functionName();
```

### Passing Values to Functions with Arguments
**Parameters** are variables that act as placeholders for the values that are to be input to a function when it is called. 

When a function is defined, it is typically defined along with one or more parameters. The actual values that are input (or "passed") into a function when it is called are known as **arguments**.

```
function testFun(param1, param2) {
  console.log(param1, param2);
}

testFun("Hello", "World");
```

### Global Scope
In JavaScript, scope refers to the **visibility of variables**. Variables which are defined outside of a function block have **Global scope**. This means, they can be seen **everywhere** in your JavaScript code.

### Local Scope
Variables which are declared within a function, as well as the function parameters have local scope. That means, they are only visible within that function.

```
function myTest() {
  var loc = "foo";
  console.log(loc);
}
myTest(); // "foo"
console.log(loc); // "undefined"
```
**Declaring a variable inside a function without VAR will create it in a Global scope !!!**

It is possible to have both local and global variables with the same name. When you do this, the local variable takes precedence over the global variable. BUT DO NOT!!!

### Return a Value from a Function with Return, and assign to a variable 
We can pass values into a function with arguments. You can use a return statement to send a value back out of a function.

```
function plusThree(num) {
  return num + 3;
}
var answer = plusThree(5); // 8
```

## Queue
In Computer Science a queue is an abstract Data Structure where items are kept in order. New items can be added at the back of the queue and old items are taken off from the front of the queue.

## Boolean values
```
true
false
```

```
function isEqual(a,b) {
  return a === b;
}
```


## Conditional Logic with If Statements
```
if (condition is true) {
  statement is executed
}
```

```
function test (myCondition) {
  if (myCondition) {
     return "It was true";
  }
  return "It was false";
}
test(true);  // returns "It was true"
test(false); // returns "It was false"
```
## Early Pattern
```
function myFun() {
  console.log("Hello");
  return "World";
  console.log("byebye")
}
myFun();
```
The above outputs "Hello" to the console, returns "World", but "byebye" is never output, because the function exits at the return statement.

## Comparison Operators

* equality operator `==`
* strict equality operator `===`
* Inequality Operator `!=`
* Strict Inequality Operator `!==`
* Greater Than Operator `>`
* Greater Than Or Equal To Operator `>=`
*  Less Than Operator `<`
* Less Than Or Equal To Operator `<=`
* Logical And Operator `&&`
* Logical Or Operator `||`


```
1   ==  1    // true
1   ==  2    // false
1   == '1'   // true
"3"  ==  3    // true

3 === 3   // true
3 === '3' // false

1 != 2      // true
1 != "1"    // false
1 != '1'    // false
1 != true   // false
0 != false  // false

3 !== 3   // false
3 !== '3' // true
4 !== 3   // true

 5 > 3   // true
 7 > '3' // true
 2 > 3   // false
'1' > 9  // false

 6  >=  6  // true
 7  >= '3' // true
 2  >=  3  // false
'7' >=  9  // false

  2 < 5  // true
'3' < 7  // true
  5 < 5  // false
  3 < 2  // false
'8' < 4  // false

  4 <= 5  // true
'7' <= 7  // true
  5 <= 5  // true
  3 <= 2  // false
'8' <= 4  // false

++++++++++++++++++++++++++++
if (num > 5 && num < 10) {
  return "Yes";
}
return "No";
++++++++++++++++++++++++++++
if (num > 10 || num < 5) {
  return "No";
}
return "Yes";

```

## Else if and Else Statements
```
if (num > 15) {
  return "Bigger than 15";
} else if (num < 5) {
  return "Smaller than 5";
} else {
  return "Between 5 and 15";
}
```
## Switch Statements
If you have many options to choose from, use a switch statement. A switch statement tests a value and can have many case statements which defines various possible values. Statements are executed from the first matched case value until a break is encountered. Case values are tested with strict equality.

```
switch (val) {
  case 1:
  case 7: (can be two like this as well)
    answer = "apple";
    break;
  case 2:
    answer = "bird";
    break;
  case 3:
    answer = "cat";
    break;
  default:
	  answer = "stuff";  
}
```

## JavaScript Objects
Objects are similar to arrays, except that instead of using indexes to access and modify their data, you access the data in objects through what are called **properties**.

```
var cat = {
  "name": "Whiskers",
  "legs": 4,
  "tails": 1,
  "enemies": ["Water", "Dogs"]
};
```
### Accessing Objects Properties 
1. Dot Operator
2. Bracket Notation
3. Variables


**.DOT**
```
var myObj = {
  prop1: "val1",
  prop2: "val2"
};
var prop1val = myObj.prop1; // val1
var prop2val = myObj.prop2; // val2
```

**[ ] BRACKET** - If the property of the object you are trying to access has a space in it, you will need to use bracket notation.
```
var myObj = {
  "Space Name": "Kirk",
  "More Space": "Spock"
};
myObj["Space Name"]; // Kirk
myObj['More Space']; // Spock
```

**Variables**
```
var someProp = "propName";
var myObj = {
  propName: "Some Value"
}
myObj[someProp]; // "Some Value"
```

## Updating properties

```
var ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};

ourDog.name = "bow-wow";
```

## Adding properties

```
var ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};

ourDog.bark = "bow-wow";
```
## Deleting properties 
```
delete ourDog.bark;
```

## Using object as lookup/library/storage
```
var alpha = {
  1:"Z",
  2:"Y",
  3:"X",
  4:"W",
  ...
  24:"C",
  25:"B",
  26:"A"
};
alpha[2]; // "Y"
alpha[24]; // "C"

var value = 2;
alpha[value]; // "Y"
```

## Object methods
`.hasOwnProperty(propname) // returns true or false`

## Complex data structure JSON = JavaScript ObjectNotation
```
var ourMusic = [
  {
    "artist": "Daft Punk",
    "title": "Homework",
    "release_year": 1997,
    "formats": [ 
      "CD", 
      "Cassette", 
      "LP" ],
    "gold": true
  }
];
```
Objects hold data in a property, which has a key-value format. In the example above, "artist": "Daft Punk" is a property that has a key of "artist" and a value of "Daft Punk".

### Accessing Nested Objects
The sub-properties of objects can be accessed by chaining together the dot or bracket notation.
```
var ourStorage = {
  "desk": {
    "drawer": "stapler"
  },
  "cabinet": {
    "top drawer": { 
      "folder1": "a file",
      "folder2": "secrets"
    },
    "bottom drawer": "soda"
  }
};
ourStorage.cabinet["top drawer"].folder2;  // "secrets"
ourStorage.desk.drawer; // "stapler"
```
### Accessing Nested Arrays
```
var ourPets = [
  {
    animalType: "cat",
    names: [
      "Meowzer",
      "Fluffy",
      "Kit-Cat"
    ]
  },
  {
    animalType: "dog",
    names: [
      "Spot",
      "Bowser",
      "Frankie"
    ]
  }
];
ourPets[0].names[1]; // "Fluffy"
ourPets[1].names[0]; // "Spot"
```

## Iterations with JavaScript _For Loops_
```
for ([initialization]; [condition]; [final-expression])
```
1. initialization is evaluated on condition start 
2. condition is evaluated at the start of every loop and make it run as long as it is true
3. final condition is checked at the end of the loop, usually to change the value that will change the loop, e.g. i++
```
var ourArray = [];
for (var i = 0; i < 5; i++) {
  ourArray.push(i);
}

=> ourArray will now contain [0,1,2,3,4]

final-expression:
i++
i += 2
i--
i -=3
etc...
```

### Loop backwards
```
var ourArray = [];
for (var i=10; i > 0; i-=2) {
  ourArray.push(i);
}
```

### Loop over an array
```
var ourArr = [ 9, 10, 11, 12];
var ourTotal = 0;

for (var i = 0; i < ourArr.length; i++) {
  ourTotal += ourArr[i];
}
```

### Nesting for loops
```
var arr = [
  [1,2], [3,4], [5,6]
];
for (var i=0; i < arr.length; i++) {
  for (var j=0; j < arr[i].length; j++) {
    console.log(arr[i][j]);
  }
}
```

## WHILE LOOPS
Another type of JavaScript loop is called a "while loop", because it runs "while" a specified condition is true and stops once that condition is no longer true.

```
var ourArray = [];
var i = 0;
while(i < 5) {
  ourArray.push(i);
  i++;
}
```

## Number generation
### Fraction, from 0 to 1, exclusive.
```
var number = Math.random();
```
### Random Whole Numbers
```
var num = Math.floor(Math.random() * 10);
```
1. Use Math.random() to generate a random decimal.
2. Multiply that random decimal by 10.
3. Use another function, Math.floor() to round the number down to its nearest whole number
4. It gives from 0 to 9 inclusive

### Generate numbers within a Range (min to max inclusive)
```
var number Math.floor(Math.random() * (max - min + 1)) + min
```
## Regular expressions
Regular expressions are used to find certain words or patterns inside of strings. For example, if we wanted to find the word the in the string The dog chased the cat, we could use the following regular expression: /the/gi

Let's break this down a bit:

1. `/` is the start of the regular expression.
2. `the` is the pattern we want to match.
3. `/` is the end of the regular expression.
4. `g` means global, which causes the pattern to return all matches in the string, not just the first one.
5. `i` means that we want to ignore the case (uppercase or lowercase) when searching for the pattern.
6.  `\s` to find whitespace in a string.
7.  `\d` to find digits
8.  You can invert any match by using the uppercase version of the regular expression selector. For example, `\s` will match any whitespace, and `\S` will match anything that isn't whitespace.

```
var testString = "There are 3 cats but 4 dogs.";
var expression = /\d+/g; 
var digitCount = testString.match(expression).length;
=> 2
var digitCount = testString.match(expression).;
=> ["3","4"]
```

### Whitespace characters
```
" " (space)
\r (the carriage return)
\n (newline)
\t (tab)
\f the form feed)

var spaceCount = testString.match(expression).length;
=> 6
```

FIND MORE INFO ABOUT

1. If you do a mathematical operation on an undefined variable your result will be NaN which means "Not a Number". If you concatenate a string with an undefined variable, you will get a literal string of "undefined".
4