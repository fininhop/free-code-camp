# Caesars Cipher

### Challenge:

	* One of the simplest and most widely known ciphers is a Caesar cipher, also known as a shift cipher. 
	* A common modern use is the ROT13 cipher, where the values of the letters are shifted by 13 places. Thus 'A' ↔ 'N', 'B' ↔ 'O' and so on.
	* Write a function which takes a ROT13 encoded string as input and returns a decoded string.
	* All letters will be uppercase. Do not transform any non-alphabetic character (i.e. spaces, punctuation), but do pass them on.
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [String.prototype.charCodeAt()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt)
  
  2 . [String.fromCharCode()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)
  
  3 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)

### I add:

  1 . [String.prototype.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)
  
  2 . [Array.prototype.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
  
  3 . [Object.RegExp()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)
  
  4 . [RegExp.prototype[@@match]()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/@@match)

### Initial code:

```javascript
function rot13(str) { // LBH QVQ VG!
  
  return str;
}

// Change the inputs below to test
rot13("SERR PBQR PNZC");
```

### My solution:

[Live Example](https://jsfiddle.net/fininhop/r6fdgca5/)

```javascript
function rot13(str) { // LBH QVQ VG!
  var strReturn = '';
  var charCodeVal;
  
  str.split('').map(function(val){
    
    if(val.match(/\W|\_|\s/) === null){
      charCodeVal = val.charCodeAt();
      
      if(charCodeVal > 77)
        strReturn += String.fromCharCode(charCodeVal-13);
      else
        strReturn += String.fromCharCode(charCodeVal+13);
      
    }else{
      strReturn += val;
    }
    
  });
  
  return strReturn;
}

// Change the inputs below to test
rot13("SERR PBQR PNZC");
```

### Explanation:
_The use of_
[Array.prototype.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) 
_is already explained before in another challenge:_ 
[find-the-longest-word-in-a-string >>Third Step  ](https://github.com/fininhop/free-code-camp/blob/master/algorithms/basic-algorithm-scripting/find-the-longest-word-in-a-string.md#third)

_Somehow,_
[Array.prototype.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) 
_is just a way to iterate through each element of an_ [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array).

_Other ways of doing the same would be using:_

[forEach()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach), [for()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for),
[while()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while)


##### Steps : 

##### Regular expression >> Description:

_Remember: To test your regular expressions, you can use websites like:_ https://regex101.com_, https://regexr.com

```javascript
/*

/\W|\_|\s/

\W = match any non-word character [^a-zA-Z0-9_]
\_ = matches the character _ literally
\s = match any white space character

*/
```

###### First : 
```javascript
// Transform the argument (str), into an array using the method split().
// And iterate through each element (val) of this array, using the method map().
str.split('').map(function(val){
```

###### Second:
```javascript
// Using the regular expression explained above, along with the method match(), to knows if the current character is a word character.
if(val.match(/\W|\_|\s/) === null){
```

###### Third:
To understand better:
The letter (A) capitalized, is code number 65;
The letter (Z) capitalized, is code number 90;

See this live-example: [Caesars Cipher - help](https://jsfiddle.net/fininhop/cn016cy9/)

```javascript
// The charCodeAt() method returns an integer between 0 and 65535 representing the UTF-16 code unit at the given index.
// For example:
// 'ABC'.charCodeAt(0); // returns 65

// Therefore, use the charCodeAt() method, to get the character code of the current character (val).
charCodeVal = val.charCodeAt();
```

###### Fourth:
```javascript
// From the letter (N) to the letter (Z). We have 13 characters.
// So, if the current character is greater than the letter (N) capitalized.
// For example:
// The character (M) has the code number 78.
// So: 78-13 = 65 (A).
if(charCodeVal > 77)
  strReturn += String.fromCharCode(charCodeVal-13);

// But, if the current character is less than the letter (N) capitalized.
// Contrary to decrease (-13) of the current code, is added (+13).
// For example:
// The character (N) has the code number 77.
// So: 77+13 = 90 (Z).

// This is because if the current character is greater than 77 (N). 
// And that adds 13 to the number of current character. 
// Then the required character would be greater than the letter (Z). Returning a wrong result.

// For example:
// The character (M) has the code number 78.
// So: 78+13 = 91 ([).
else
  strReturn += String.fromCharCode(charCodeVal+13);
```

###### Fifth:
```javascript
// All non-word characters are left in their original position.
}else{
  strReturn += val;
```

###### Sixth:
```javascript
// In this example this function returns: "FREE CODE CAMP".
```
