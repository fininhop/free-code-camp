# Seek and Destroy

### Challenge:

	* You will be provided with an initial array (the first argument in the destroyer function), followed by one or more arguments.
	* Remove all elements from the initial array that are of the same value as these arguments.
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [Arguments object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments)
  
  2 . [Array.prototype.filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
  
  3 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)

### I add:

  1 . [Array.prototype.indexOf()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)

### Initial code:

```javascript
function destroyer(arr) {
  // Remove all the values
  return arr;
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```

### My solution:

[Live example](https://jsfiddle.net/fininhop/fdwtwrwh/)

```javascript
function destroyer(arr) {
  var arrToCheck = Array.prototype.slice.call(arguments[0]);
  var arrValuesToCheck = Array.prototype.slice.call(arguments, 1);
  
  return arrToCheck.filter(function(val){
    if(arrValuesToCheck.indexOf(val) === -1)
      return val;
  });
  
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```

### Explanation:

##### Steps : 
###### First : 
```javascript
// The arguments object:
// This object contains an entry for each argument passed to the function, the index of the first entry that starts at 0.

// Assuming the agument (arr), is equals to: ([1, 2, 3, 1, 2, 3], 2, 3)

// So the following array called (arrToCheck), is the same as: [1, 2, 3, 1, 2, 3]
var arrToCheck = Array.prototype.slice.call (arguments [0]);

// And the next array called (arrValuesToCheck) is the same as: [2,3]
var arrValuesToCheck = Array.prototype.slice.call(arguments, 1);
```

###### Second:

_The method_ [Array.prototype.filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter), _was also used in this another challenge:_ [Falsy Bouncer>> Explanation](https://github.com/fininhop/free-code-camp/blob/master/algorithms/basic-algorithm-scripting/falsy-bouncer.md#explanation)

```javascript
// The filter() method creates a new array with all elements that pass the test implemented by the provided function.
// The parameter callback test each element (val), of the array (arrToCheck).
return arrToCheck.filter(function(val){
```

###### Third:
```javascript
//The Array.prototype.indexOf() return (-1) if the item sought is not found.
//So for each item (val) in the array (arrToCheck):
//If the item (val) does not exist in the array (arrValuesToCheck).
//The item (val) is added to the array, which will return the method filter().
if(arrValuesToCheck.indexOf(val) === -1)
  return val;
```
