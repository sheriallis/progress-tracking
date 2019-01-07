# Basic Algorithm Scripting

## Convert Celsius to Fahrenheit

The algorithm to convert from Celsius to Fahrenheit is the temperature in Celsius times 9/5, plus 32.

You are given a variable celsius representing a temperature in Celsius. Use the variable fahrenheit already defined and assign it the Fahrenheit temperature equivalent to the given Celsius temperature. Use the algorithm mentioned above to help convert the Celsius temperature to Fahrenheit.

```js
function convertToF(celsius) {
  let fahrenheit = celsius * 9 / 5 + 32;
  return fahrenheit;
}

convertToF(20);
```

## Reverse a String

Reverse the provided string.

```js
function reverseString(str) {
  return str
    .split("")
    .reverse()
    .join("");
}

reverseString("hello");
```

## Factorialize a Number

Return the factorial of the provided integer.

If the integer is represented with the letter n, a factorial is the product of all positive integers less than or equal to n.

```js
function factorialize(num) {
  if (num <= 0) {
    return 1;
  } else {
    return num * factorialize(num - 1);
  }
}

factorialize(20);
```

## Find the Longest Word in a String

Return the length of the longest word in the provided sentence.

Your response should be a number.

```js
function findLongestWordLength(str) {
  let wordLength = str.split(" ").map(word => word.length);
  return Math.max(...wordLength);
}

findLongestWordLength("The quick brown fox jumped over the lazy dog");
```

## Return Largest Numbers in Arrays

Return an array consisting of the largest number from each provided sub-array. For simplicity, the provided array will contain exactly 4 sub-arrays.

```js
function largestOfFour(arr) {
  return arr.map(subArr => Math.max(...subArr));
}

largestOfFour([
  [4, 5, 1, 3],
  [13, 27, 18, 26],
  [32, 35, 37, 39],
  [1000, 1001, 857, 1]
]);
```

## Confirm the Ending

Check if a string (first argument, str) ends with the given target string (second argument, target).

This challenge can be solved with the .endsWith() method, which was introduced in ES2015. But for the purpose of this challenge, we would like you to use one of the JavaScript substring methods instead.

```js
function confirmEnding(str, target) {
  // "Never give up and good luck will find you."
  // -- Falcor
  return str.substring(str.length - target.length) === target ? true : false;
}

confirmEnding("Bastian", "n"); // should return true
confirmEnding("He has to give me a new name", "name"); // should return true
confirmEnding(
  "If you want to save our world, you must hurry. We dont know how much longer we can withstand the nothing",
  "mountain"
); // should return false
```

## Repeat a String Repeat a String

Repeat a given string str (first argument) for num times (second argument). Return an empty string if num is not a positive number.

The built-in repeat()-method should not be used

```js
function repeatStringNumTimes(str, num) {
  let repeated = "";

  if (num < 0) {
    return "";
  }

  for (let i = 0; i < num; i++) {
    repeated += str;
  }
  return repeated;
}

repeatStringNumTimes("abc", 7);
```

## Truncate a String

Truncate a string (first argument) if it is longer than the given maximum string length (second argument). Return the truncated string with a ... ending.

```js
function truncateString(str, num) {
  // Clear out that junk in your trunk
  return str.length > num ? str.slice(0, num) + "..." : str;
}

truncateString("A-tisket a-tasket A green and yellow basket", 8);
```

## Finders Keepers

Create a function that looks through an array (first argument) and returns the first element in the array that passes a truth test (second argument). If no element passes the test, return undefined.

```js
function findElement(arr, func) {
  for (let i = 0; i < arr.length; i++) {
    if (func(arr[i])) {
      return arr[i];
    }
  }
}

findElement([1, 2, 3, 4], num => num % 2 === 0);
```

## Boo who

Check if a value is classified as a boolean primitive. Return true or false.

```js
function booWho(bool) {
  // What is the new fad diet for ghost developers? The Boolean.
  return typeof bool === "boolean";
}

booWho(null);
```

## Title Case a Sentence

Return the provided string with the first letter of each word capitalized. Make sure the rest of the word is in lower case.

```js
function titleCase(str) {
  return str.toLowerCase().replace(/(^|\s)\S/g, letter => letter.toUpperCase());
}

titleCase("I'm a little tea pot");
```

## Falsy Bouncer

```js
function bouncer(arr) {
  return arr.filter(Boolean);
}

bouncer([7, "ate", "", false, 9]);
```

## Where do I Belong

Return the lowest index at which a value (second argument) should be inserted into an array (first argument) once it has been sorted. The returned value should be a number.

For example, getIndexToIns([1,2,3,4], 1.5) should return 1 because it is greater than 1 (index 0), but less than 2 (index 1).

Likewise, getIndexToIns([20,3,5], 19) should return 2 because once the array has been sorted it will look like [3,5,20] and 19 is less than 20 (index 2) and greater than 5 (index 1).

```js
function getIndexToIns(arr, num) {
  arr.push(num);
  return arr.sort((a, b) => a - b).indexOf(num);
}

getIndexToIns([3, 10, 5], 3);
```
