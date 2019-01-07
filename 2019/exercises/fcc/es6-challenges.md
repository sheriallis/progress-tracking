# Javascript Algorithms And Data Structures: ES6

## Use Destructuring Assignment to Assign Variables from Objects

Use destructuring to obtain the length of the input string str, and assign the length to len in line.

```js
function getLength(str) {
  "use strict";

  // change code below this line
  const { length: len } = str; // change this
  // change code above this line

  return len; // you must assign length to len in line
}

console.log(getLength("FreeCodeCamp"));
```

## Use Destructuring Assignment to Pass an Object as a Function's Parameters

Use destructuring assignment within the argument to the function half to send only max and min inside the function.

```js
const stats = {
  max: 56.78,
  standard_deviation: 4.34,
  median: 34.54,
  mode: 23.87,
  min: -0.75,
  average: 35.85
};
const half = (function() {
  "use strict"; // do not change this line

  // change code below this line
  return function half({ max, min }) {
    // use function argument destructuring
    return (max + min) / 2.0;
  };
  // change code above this line
})();
console.log(stats); // should be object
console.log(half(stats)); // should be 28.015
```

## Create Strings using Template Literals

Use template literal syntax with backticks to display each entry of the result object's failure array. Each entry should be wrapped inside an li element with the class attribute text-warning, and listed within the resultDisplayArray.

```js
const result = {
  success: ["max-length", "no-amd", "prefer-arrow-functions"],
  failure: ["no-var", "var-on-top", "linebreak"],
  skipped: ["id-blacklist", "no-dup-keys"]
};
function makeList(arr) {
  "use strict";

  // change code below this line
  const resultDisplayArray = arr.map(warning => {
    return `<li class="text-warning">${warning}</li>`;
  });
  // change code above this line

  return resultDisplayArray;
}
/**
 * makeList(result.failure) should return:
 * [ <li class="text-warning">no-var</li>,
 *   <li class="text-warning">var-on-top</li>,
 *   <li class="text-warning">linebreak</li> ]
 **/
const resultDisplayArray = makeList(result.failure);
```

## Write Concise Object Literal Declarations Using Simple Fields

Use simple fields with object literals to create and return a Person object.

```js
const createPerson = (name, age, gender) => {
  "use strict";
  // change code below this line
  return {
    name,
    age,
    gender
  };
  // change code above this line
};
console.log(createPerson("Zodiac Hasbro", 56, "male"));
```

## Write Concise Declarative Functions with ES6

Refactor the function setGear inside the object bicycle to use the shorthand syntax described above.

```js
const bicycle = {
  gear: 2,
  setGear(newGear) {
    "use strict";
    this.gear = newGear;
  }
};
// change code above this line
bicycle.setGear(3);
console.log(bicycle.gear);
```

## Use class Syntax to Define a Constructor Function

Use class keyword and write a proper constructor to create the Vegetable class.

The Vegetable lets you create a vegetable object, with a property name, to be passed to constructor.

```js
function makeClass() {
  "use strict";
  /* Alter code below this line */
  class Vegetable {
    constructor(name) {
      this.name = name;
    }
  }
  /* Alter code above this line */
  return Vegetable;
}
const Vegetable = makeClass();
const carrot = new Vegetable("carrot");
console.log(carrot.name); // => should be 'carrot'
```

## Use getters and setters to Control Access to an Object

Use class keyword to create a Thermostat class. The constructor accepts Farenheit temperature.

Now create getter and setter in the class, to obtain the temperature in Celsius scale.

Remember that C = 5/9 _ (F - 32) and F = C _ 9.0 / 5 + 32, where F is the value of temperature in Fahrenheit scale, and C is the value of the same temperature in Celsius scale

**Note:** When you implement this, you would be tracking the temperature inside the class in one scale - either Fahrenheit or Celsius.

This is the power of getter or setter - you are creating an API for another user, who would get the correct result, no matter which one you track.

In other words, you are abstracting implementation details from the consumer.

```js
function makeClass() {
  "use strict";
  /* Alter code below this line */
  class Thermostat {
    constructor(temperature) {
      this._temperature = temperature;
    }
    get temp() {
      return this._temperature;
    }

    set temp(fahr) {
      this._temperature = 5 / 9 * (fahr - 32);
    }
  }
  /* Alter code above this line */
  return Thermostat;
}
const Thermostat = makeClass();
const thermos = new Thermostat(76); // setting in Farenheit scale
let temp = thermos.temperature; // 24.44 in C
thermos.temperature = 26;
temp = thermos.temperature; // 26 in C
```
