# Check for Palindromes

### Challenge:

	* Return true if the given string is a palindrome. Otherwise, return false.
	* A palindrome is a word or sentence that's spelled the same way both forward and backward, ignoring punctuation, case, and spacing.
	* Your result must be a string.
	* Note
	* You'll need to remove all non-alphanumeric characters (punctuation, spaces and symbols) and turn everything lower case in order to check for palindromes.
	* We'll pass strings with varying formats, such as "racecar", "RaceCar", and "race CAR" among others.
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [String.replace()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace)
  
  2 . [String.toLowerCase()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase)
  
  3 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)
  
### I add:

  1 . [Object.RegExp()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

### Initial code:

```javascript
function palindrome(str) {
  // Good luck!
  return true;
}

palindrome("eye");
```

### My solution:

[Live example](https://jsfiddle.net/fininhop/a60q6o9n/)

```javascript
function palindrome(str) {
  var strReverse;
  
  str = str.toLowerCase().replace(/\W|\_|\s/g, '');
  strReverse = str.split('').reverse().join('');
  
  if(strReverse === str)
    return true;
  else
    return false;
}

palindrome("eye");
```

### Explanation:
_Remember: To test your regular expressions, you can use websites like:_ https://regex101.com_, https://regexr.com

##### Regular expression >> Description:
```javascript
/*
  /\W|\_|\s/g
  
  \W = match any non-word character [^a-zA-Z0-9_]
  \_ = matches the character _ literally
  \s = match any white space character
  g modifier: global. All matches (don't return on first match)_
*/
```
##### Steps: 

###### First: 
```javascript
//Make the string lower case.
//To find and remove all matches:
//Use the javascript replace() method, with the previously explained regular expression as parameter.

str = str.toLowerCase().replace(/\W|\_|\s/g, '');
```

###### Second: 

_Already been explained._ >> [Reverse a String](https://github.com/fininhop/free-code-camp/blob/master/algorithms/reverse-a-string.md)

```javascript
//Reverse the string

strReverse = str.split('').reverse().join('');
```

###### Third: 
```javascript
//If the reversed string, is equal to the original string. This word is a palindrome.

if(strReverse === str)
  return true;
else
  return false;
```
