# Falsy Bouncer

### Challenge:

	* Remove all falsy values from an array.
	* Falsy values in JavaScript are false, null, 0, "", undefined, and NaN.
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [Boolean Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)
  
  2 . [Array.prototype.filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
  
  3 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)

### Initial code:

```javascript
function bouncer(arr) {
  // Don't show a false ID to this bouncer.
  return arr;
}

bouncer([7, "ate", "", false, 9]);
```

### My solution:
#### Solution n°1:

[Live example](https://jsfiddle.net/fininhop/cwuyc3d3/)

```javascript
function filterResults(val){
  return Boolean(val);
}

function bouncer(arr) {
  return arr.filter(filterResults);
}

bouncer([7, "ate", "", false, 9]);
```

#### Solution n°2:

[Live Example](https://jsfiddle.net/fininhop/zboypj7d/)

```javascript
function bouncer(arr) {
  return arr.filter(function(val){
    return Boolean(val);
  });
}

bouncer([7, "ate", "", false, 9]);
```

### Explanation:
_Both solutions do exactly the same thing._

_As we can see in the second example. It is possible to call the callback function, without declaring another function to do that._

##### Steps : 
###### First : 
```javascript
//The Array.prototype.filter() method returns a new array.
//For each element of the argument (arr).
//If the boolean object of the callback function return a true value.
//The element is added into the new array.
//Otherwise not.

function bouncer(arr) {
  return arr.filter(function(val){
```

###### Second:
```javascript
//Boolean object - Description
//The value passed as the first parameter is converted to a boolean value, if necessary. 
//If value is omitted or is 0, -0, null, false, NaN, undefined, or the empty string (""), the object has an initial value of false.
//All other values, including any object or the string "false", create an object with an initial value of true.
return Boolean(val);
```

###### Third:
```javascript
//This function returns, the resulting array of the Array.prototype.filter() method.
//In this example this would be:  [7, "ate", 9];
```
