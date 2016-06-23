# Confirm the Ending

### Challenge:

	* Check if a string (first argument, str) ends with the given target string (second argument, target).
	* This challenge can be solved with the .endsWith() method, which was introduced in ES2015.
	* But for the purpose of this challenge, we would like you to use one of the JavaScript substring methods instead.
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [String.prototype.substr()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substr)
  
  2 . [String.prototype.substring()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substring)
  
  3 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)
  

### Initial code:

```javascript
function confirmEnding(str, target) {
  // "Never give up and good luck will find you."
  // -- Falcor
  return str;
}

confirmEnding("Bastian", "n");
```

### My solution:

[Live example](https://jsfiddle.net/fininhop/3v060ksx/)

```javascript
function confirmEnding(str, target) {
  
  if(target === str.substr(-target.length))
    return true;  
  else
    return false;
  
}

confirmEnding("Bastian", "n");
```

### Explanation:

_I think the code is self explanatory._

```javascript
//Use of the substr() method. To get the last element of the string of chars.
str.substr(-target.length)

//Compare this value with the target value.
//Then return, true or false depending the result of the comparison.
if(target === str.substr(-target.length))
  return true;  
else
  return false;

```

##### Additional 

_This challenge can be solved with the_ [String.prototype.endsWith()](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/String/endsWith) _method, which was introduced in ES2015._

###### Example:
[Live example](https://jsfiddle.net/fininhop/u1yhr1yt/)
```javascript
function confirmEnding(str, target) {
  return str.endsWith(target);
}

confirmEnding("Bastian", "n");
```

