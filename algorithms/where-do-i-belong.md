# Where do I belong

### Challenge:

	* Return the lowest index at which a value (second argument) should be inserted into an array (first argument) once it has been sorted. 
	* The returned value should be a number.
	* For example, getIndexToIns([1,2,3,4], 1.5) should return 1 because it is greater than 1 (index 0), but less than 2 (index 1).
	* Likewise, getIndexToIns([20,3,5], 19) should return 2 because once the array has been sorted it will look like [3,5,20] and 19 is less than 20 (index 2) and greater than 5 (index 1).
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [Array.prototype.sort()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
  
  2 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)

### I add:
  
  1 . [Array.prototype.push()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)

  2 . [Array.prototype.indexOf()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)

### Initial code:

```javascript
function getIndexToIns(arr, num) {
  // Find my place in this sorted array.
  return num;
}

getIndexToIns([40, 60], 50);
```

### My solution:

[Live example](https://jsfiddle.net/fininhop/53jw943r/)

```javascript
function getIndexToIns(arr, num) {
  arr.push(num);
  
  arr.sort(function(a, b){
    return (a - b);
  });
  
  return arr.indexOf(num);
}

getIndexToIns([40, 60], 50);
```

### Explanation:

##### Steps : 
###### First : 
```javascript
// Put the first argument named (num), in the second argument named (arr).
arr.push(num);
```

###### Second:
```javascript
// The sort() method, sorts the elements of the array named (arr), and returns an ordered array.
// To compare numbers instead of strings, the compare function can simply subtract a from b.
// The following function will sort the array ascending:
arr.sort(function(a, b){
  return (a - b);
});
```

###### Third:
```javascript
// Make use of the method indexOf(), to locate the position of the argument named (num), in the ordered array returned by the method sort().
return arr.indexOf(num);
```
