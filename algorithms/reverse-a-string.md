# Reverse a String

### Challenge:

	* Reverse the provided string.
	* You may need to turn the string into an array before you can reverse it.
	* Your result must be a string.
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [Global String Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
  
  2 . [String.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)
  
  3 . [Array.reverse()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse)
  
  4 . [Array.join()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)
  
  5 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)

### Initial code:

```javascript
function reverseString(str) {
  return str;
}

reverseString("hello");
```

### My solution:
#### Solution n°1:

[Live example](https://jsfiddle.net/fininhop/bzpz9bLg/1/)

```javascript
function reverseString(str) {
  var arrStr = str.split('');
  
  arrStr = arrStr.reverse();
  str = arrStr.join('');
  return str;
}

reverseString("hello");
```

#### Solution n°2:

[Live Example](https://jsfiddle.net/fininhop/uytyzh6u/)

```javascript
function reverseString(str) {
  return str.split('').reverse().join('');
}

reverseString("hello");
```

### Explanation:
_Both solutions do exactly the same thing._

_As we can see in the second example. It is possible to do all the actions in the first example. Simply using a single line of code._

##### Steps : 
###### First : 
```javascript
//Transform the string of chars into an array. 
var arrStr = str.split('');
```

###### Second:
```javascript
//Reverse the resulting array.
arrStr = arrStr.reverse();
```

###### Third:
```javascript
//Join the elements of the resulting reversed array, into a new string of chars.
str = arrStr.join('');
```
