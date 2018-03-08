# es6-exercises

### Modify the following code to use var, const, and let appropriately. Replace the underlines with either 'var', 'const', or 'let'

```js
const SPEED_OF_LIGHT = 299792458

var speedArray = [55, 9.8, 1000000000, 186300]

for (let i = 0; i < speedArray.length; i++) {
  if (speedArray[i] > SPEED_OF_LIGHT) {
    console.log("Faster than light")
  } else {
    console.log("Sub-light speed")
  }
}
```

### What errors will the following code blocks produce? Why?

```js - ANSWER: We are trying to change the value of a constant which is immutable! ninja turtles
const foo = 5;
foo = 6;
```

```js - ANSWER: Will error on console.log(bar) because it only exists in the if code block
var foo = 5;
if (foo > 3) {
  let bar = 2;
  foo = foo * bar;
}
console.log(foo);
console.log(bar);
```
```js
const farge = {
  prop1: "one",
  prop2: "two",
  prop3: "three"
}
farge = {newProp: "new"};  // ANSWER: ERROR! - trying to assign new value to a constnat
farge.prop1 = "forty-two"; // ANSWER: No Error - can alter a object value even with const
farge.propX = "ex";        // ANSWER: No Error - will add new property to farge
delete farge.propX;        // ANSWER: No Error - allowed to alter object
console.log(farge);
```


### Rewrite the following functions using arrow functions

```js
var adder = function(a, b) {
  return a + b;
}

ANSWER: adder = (a, b) => a + b

```
```js
function printFarge() {
  console.log('farge');
}

ANSWER: printFarge = () => console.log('farge')

```
```js
var cleanTheString = function(str) {
  let newStr = str.replace(/\s/g, '');
  newStr = newStr.toUpperCase();
  return newStr;
}

ANSWER: cleanTheString = (str) => {
  let newStr = str.replace(/\s/g, '')
  newStr = newStr.toUpperCase();
  return newStr;
}

```

### Use Object Literal shorthand to clean up the following code

```js
var color = "blue";
var length = 14;
var style = "Flamenco";

var widget = {
  color,
  length,
  style
}
```

### Use String Literals to make the following code more readable

```js
var name = "Paco";
var location = "Nogales";
var food = "steak";

var bio = `${name} is from ${location} and really likes to eat ${food1}`;
```

### The blocks below represent two separate files. Write out the statements needed to use the function from the first file in the code in the second file

```js
// This is in hello.js
var hello = function(name) {
  console.log(`Hello, ${name}!`);
}
export default hello

```
```js
// This is in main.js
import hello from './hello'

hello("Siouxsie");
```
