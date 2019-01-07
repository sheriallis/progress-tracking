# Javascript Algorithms And Data Structures: Regular Expressions

## Using the Test Method

Apply the regex myRegex on the string myString using the .test() method.

```js
let myString = "Hello, World!";
let myRegex = /Hello/;
let result = myRegex.test(myString);
```

## Match Literal Strings

Complete the regex waldoRegex to find "Waldo" in the string waldoIsHiding with a literal match.

```js
let waldoIsHiding = "Somewhere Waldo is hiding in this text.";
let waldoRegex = /Waldo/;
let result = waldoRegex.test(waldoIsHiding);
```

## Match a Literal String with Different Possibilities

Complete the regex petRegex to match the pets "dog", "cat", "bird", or "fish".

```js
let petString = "James has a pet cat.";
let petRegex = /dog|cat|bird|fish/;
let result = petRegex.test(petString);
```

## Ignore Case While Matching

Write a regex fccRegex to match "freeCodeCamp", no matter its case. Your regex should not match any abbreviations or variations with spaces.

```js
let myString = "freeCodeCamp";
let fccRegex = /freecodecamp/i;
let result = fccRegex.test(myString);
```

## Extract Matches

Apply the .match() method to extract the word coding.

```js
let extractStr = "Extract the word 'coding' from this string.";
let codingRegex = /coding/;
let result = extractStr.match(codingRegex);
```

## Find More Than the First Match

Using the regex starRegex, find and extract both "Twinkle" words from the string twinkleStar.

```js
let twinkleStar = "Twinkle, twinkle, little star";
let starRegex = /Twinkle/gi;
let result = twinkleStar.match(starRegex);
```

## Match Anything with Wildcard Period

Complete the regex unRegex so that it matches the strings "run", "sun", "fun", "pun", "nun", and "bun". Your regex should use the wildcard character.

```js
let exampleStr = "Let's have fun with regular expressions!";
let unRegex = /.un/;
let result = unRegex.test(exampleStr);
```

## Match Single Character with Multiple Possibilities

Use a character class with vowels (a, e, i, o, u) in your regex vowelRegex to find all the vowels in the string quoteSample.

```js
let quoteSample =
  "Beware of bugs in the above code; I have only proved it correct, not tried it.";
let vowelRegex = /[aeiou]/gi;
let result = quoteSample.match(vowelRegex);
```

## Match Letters of the Alphabet

Match all the letters in the string quoteSample. **Be sure to match both upper- and lowercase vowels.**

```js
let quoteSample = "The quick brown fox jumps over the lazy dog.";
let alphabetRegex = /[a-z]/gi;
let result = quoteSample.match(alphabetRegex);
```

## Match Numbers and Letters of the Alphabet

Create a single regex that matches a range of letters between h and s, and a range of numbers between 2 and 6. Remember to include the appropriate flags in the regex.

```js
let quoteSample = "Blueberry 3.141592653s are delicious.";
let myRegex = /[h-s2-6]/gi;
let result = quoteSample.match(myRegex);
```

## Match Single Characters Not Specified

Create a single regex that matches all characters that are not a number or a vowel. Remember to include the appropriate flags in the regex.

```js
let quoteSample = "3 blind mice.";
let myRegex = /[^aiueo0-9]/gi;
let result = quoteSample.match(myRegex);
```

## Match Characters that Occur One or More Times

You want to find matches when the letter s occurs one or more times in "Mississippi". Write a regex that uses the + sign.

```js
let difficultSpelling = "Mississippi";
let myRegex = /s+/gi;
let result = difficultSpelling.match(myRegex);
```

## Match Characters that Occur Zero or More Times

Create a regex chewieRegex that uses the \* character to match all the upper and lower"a" characters in chewieQuote. Your regex does not need flags, and it should not match any of the other quotes.

```js
let chewieQuote = "Aaaaaaaaaaaaaaaarrrgh!";
let chewieRegex = /Aa*/;
let result = chewieQuote.match(chewieRegex);
```

## Find Characters with Lazy Matching

Fix the regex /<.\*>/ to return the HTML tag <h1> and not the text "<h1>Winter is coming</h1>". Remember the wildcard . in a regular expression matches any character.

```js
let text = "<h1>Winter is coming</h1>";
let myRegex = /<h?.>/; // Change this line
let result = text.match(myRegex);
```

## Find One or More Criminals in a Hunt

Write a greedy regex that finds one or more criminals within a group of other people. A criminal is represented by the capital letter C.

```js
// example crowd gathering
let crowd = "P1P2P3P4P5P6CCCP7P8P9";

let reCriminals = /C+/; // Change this line

let matchedCriminals = crowd.match(reCriminals);
console.log(matchedCriminals);
```

## Match Beginning String Patterns

Use the caret character in a regex to find "Cal" only in the beginning of the string rickyAndCal.

```js
let rickyAndCal = "Cal and Ricky both like racing.";
let calRegex = /^Cal/; // Change this line
let result = calRegex.test(rickyAndCal);
```

## Match Ending String Patterns

Use the anchor character ($) to match the string "caboose" at the end of the string caboose.

```js
let caboose = "The last car on a train is the caboose";
let lastRegex = /caboose$/; // Change this line
let result = lastRegex.test(caboose);
```

## Match All Letters and Numbers

Use the shorthand character class \w to count the number of alphanumeric characters in various quotes and strings.

```js
let quoteSample = "The five boxing wizards jump quickly.";
let alphabetRegexV2 = /\w/g;
let result = quoteSample.match(alphabetRegexV2).length;
```

## Match Everything But Letters and Numbers

Use the shorthand character class \W to count the number of non-alphanumeric characters in various quotes and strings.

```js
let quoteSample = "The five boxing wizards jump quickly.";
let nonAlphabetRegex = /\W/g; // Change this line
let result = quoteSample.match(nonAlphabetRegex).length;
```

## Match All Numbers

Use the shorthand character class \d to count how many digits are in movie titles. Written out numbers ("six" instead of 6) do not count.

```js
let numString = "Your sandwich will be $5.00";
let numRegex = /\d/g;
let result = numString.match(numRegex).length;
```

## Match All Non-Numbers

Use the shorthand character class for non-digits \D to count how many non-digits are in movie titles.

```js
let numString = "Your sandwich will be $5.00";
let noNumRegex = /\D/g;
let result = numString.match(noNumRegex).length;
```

## Restrict Possible Usernames

Usernames are used everywhere on the internet. They are what give users a unique identity on their favorite sites.

You need to check all the usernames in a database. Here are some simple rules that users have to follow when creating their username.

1.  The only numbers in the username have to be at the end. There can be zero or more of them at the end.

2.  Username letters can be lowercase and uppercase.

3.  Usernames have to be at least two characters long. A two-letter username can only use alphabet letter characters.

Change the regex userCheck to fit the constraints listed above.

```js
let username = "JackOfAllTrades";
let userCheck = /[a-zA-z]{2,}\d*$/i;
let result = userCheck.test(username);
```

## Match Whitespace

Change the regex countWhiteSpace to look for multiple whitespace characters in a string.

```js
let sample = "Whitespace is important in separating words";
let countWhiteSpace = /\s/g;
let result = sample.match(countWhiteSpace);
```

## Match Non-Whitespace Characters

Change the regex countNonWhiteSpace to look for multiple non-whitespace characters in a string.

```js
let sample = "Whitespace is important in separating words";
let countNonWhiteSpace = /\S/g;
let result = sample.match(countNonWhiteSpace);
```

## Specify Upper and Lower Number of Matches

Change the regex ohRegex to match only 3 to 6 letter h's in the word "Oh no".

```js
let ohStr = "Ohhh no";
let ohRegex = /Oh{3,6} no/;
let result = ohRegex.test(ohStr);
```

## Specify Only the Lower Number of Matches

Change the regex haRegex to match the word "Hazzah" only when it has four or more letter z's.

```js
let haStr = "Hazzzzah";
let haRegex = /Haz{4,}ah/;
let result = haRegex.test(haStr);
```

## Specify Exact Number of Matches

Change the regex timRegex to match the word "Timber" only when it has four letter m's.

```js
let timStr = "Timmmmber";
let timRegex = /Tim{4}ber/;
let result = timRegex.test(timStr);
```

## Check for All or None

Change the regex favRegex to match both the American English (favorite) and the British English (favourite) version of the word.

```js
let favWord = "favorite";
let favRegex = /favou?rite/;
let result = favRegex.test(favWord);
```

## Positive and Negative Lookahead

Use lookaheads in the pwRegex to match passwords that are greater than 5 characters long and have two consecutive digits.

```js
let sampleWord = "astronaut";
let pwRegex = /(?=\w{5,})(?=\D*\d{2})/;
let result = pwRegex.test(sampleWord);
```

## Reuse Patterns Using Capture Groups

Use capture groups in reRegex to match numbers that are repeated only three times in a string, each separated by a space.

```js
```

## Use Capture Groups to Search and Replace

Write a regex so that it will search for the string "good". Then update the replaceText variable to replace "good" with "okey-dokey".

```js
var huhText = "This sandwich is good.";
var fixRegex = /good/;
var replaceText = "okey-dokey";
var result = huhText.replace(fixRegex, replaceText);
```

## Remove Whitespace from Start and End

Write a regex and use the appropriate string methods to remove whitespace at the beginning and end of strings.

**Note:** The .trim() method would work here, but you'll need to complete this challenge using regular expressions.

```js
let hello = "   Hello, World!  ";
let wsRegex = /^\s+|\s+$/gi; // Change this line
let result = hello.replace(wsRegex, ""); // Change this line
```
