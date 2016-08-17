# Object Oriented and Functional Programming
Basic notes on objects and JSON are in Basic JavaScript notes. Objects have their own attributes, called `properties`, and their own functions, called `methods`.

## Create objects
### Using **constructor functions**
A `constructor` function is given a capitalized name to make it clear that it is a `constructor`.
```
var Car = function() {
  this.wheels = 4;
  this.engines = 1;
  this.seats = 5;
};
```
In a constructor the `this` variable refers to the new object being created by the constructor. So when we write,
```
this.wheels = 4;
```
inside of the constructor we are giving the new object it creates a property called `wheels` with a value of 4. You can think of a constructor as a description for the object it will create.

To use a constructor function we call it with the new keyword in front of it like:
```
var myCar = new Car();
```
Note that it is important to use the new keyword when calling a constructor. This is how JavaScript knows to create a new object and that all the references to `this` inside the constructor should be referring to this new object.

#### Passing Parameters to Constructor

```
var Car = function(wheels, seats, engines) {
  this.wheels = wheels;
  this.seats = seats;
  this.engines = engines;
};
```

using it

```
var myCar = new Car(6, 3, 1);

=>
{
  wheels: 6,
  seats: 3,
  engines: 1
}
```

#### Make Object Properties Private
```
var Car = function() {
  // this is a private variable
  var speed = 10;

  // these are public methods
  this.accelerate = function(change) {
    speed += change;
  };

  this.decelerate = function() {
    speed -= 5;
  };

  this.getSpeed = function() {
    return speed;
  };
};
```
## Arrays Methods

### Iterate with .map
The map method is a convenient way to iterate through arrays. Here's an example usage:
```
var oldArray = [1, 2, 3];
var timesFour = oldArray.map(function(val){
  return val * 4;
});
console.log(timesFour); // returns [4, 8, 12]
console.log(oldArray);  // returns [1, 2, 3]
```
The map method will iterate through every element of the array, creating a new array with values that have been modified by the callback function, and return it. Note that it does not modify the original array.

### Condense with .reduce
The array method `reduce` is used to iterate through an array and condense it into one value.
More info on reduce [mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce) and here: [javascript-array-reduce](https://www.airpair.com/javascript/javascript-array-reduce)

```
var singleVal = array.reduce(function(previousVal, currentVal) {
  return previousVal - currentVal;
}, 0);
```
### Filter
The filter method is used to iterate through an array and filter out elements where a given condition is not true.
```
array = array.filter(function(val) {
  return val !== 5;
});
```
### Sort (mutable)
You can use the method `sort` to easily sort the values in an array alphabetically or numerically. Unlike the previous array methods we have been looking at, sort actually alters the array in place. However, it also returns this sorted array.

`sort` can be passed a compare function as a callback. The compare function should return a negative number if `a` should be before `b`, a positive number if `a` should be after `b`, or `0` if they are equal.

If no compare (callback) function is passed in, it will convert the values to strings and sort alphabetically.
```
var array = [1, 12, 21, 2];
array.sort(function(a, b) {
  return a - b;
});
```

### Reverse (mutable)
You can use the `reverse` method to reverse the elements of an array. `reverse` is another array method that alters the array in place, but it also returns the reversed array.
```
var array = [1, 12, 21, 2];
array.reverse();

=>[2, 21, 12, 1]
```
### Concatenate
```
newArray = oldArray.concat(otherArray);
```

## Strings methods
### Split string into an array
```
var string = "Split me into an array";
var array = [];

array = string.split(" ");

["Split", "me", "into", "an", "array"]
```
### Join
```
var veggies = ["Celery", "Radish", "Carrot", "Potato"];
var salad = veggies.join(" and ");
console.log(salad); // "Celery and Radish and Carrot and Potato"
```
