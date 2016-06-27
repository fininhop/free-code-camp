# Slasher Flick

### Challenge:

	* Return the remaining elements of an array after chopping off n elements from the head.
	* The head means the beginning of the array, or the zeroth index.
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [Array.prototype.slice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)
  
  2 . [Array.prototype.splice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)
  
  3 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)

### Initial code:

```javascript
function slasher(arr, howMany) {
  // it doesn't always pay to be first
  return arr;
}

slasher([1, 2, 3], 2);
```

### My solution:

[Live example](https://jsfiddle.net/fininhop/034w4128/)

```javascript
function slasher(arr, howMany) {
  
  arr.splice(0, howMany);
  return arr;

}

slasher([1, 2, 3], 2);
```

### Explanation:

```javascript
//Simple utilization of: Array.prototype.slice () method.
//The first parameter (0), represents the index where to start the extraction of elements of the argument (arr).
//The second parameter (howMany), is the number of items that will be deleted in ascending order.
//There may be a third parameter. Although it is not necessary in this example.

//In this example, this function returns: [3];
arr.splice(0, howMany);
return arr;
```
