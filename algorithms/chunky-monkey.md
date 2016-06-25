# Chunky Monkey

### Challenge:

	* Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a two-dimensional array.
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [Array.prototype.push()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)
  
  2 . [Array.prototype.slice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)
  
  3 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)
  

### Initial code:

```javascript
function chunkArrayInGroups(arr, size) {
  // Break it up.
  return arr;
}

chunkArrayInGroups(["a", "b", "c", "d"], 2);
```

### My solution:

[Live example](https://jsfiddle.net/fininhop/2zy37zh5/)

```javascript
function chunkArrayInGroups(arr, size) {
  var arrReturn = [];
  var next = 0;
  
  for(var i = 0; i < arr.length; i++){
    
    if(next === 0 || i === next){
      arrReturn.push(arr.slice(i, i+size));
      next = i+size;
    }
    
  }
  
  return arrReturn;
}

chunkArrayInGroups(["a", "b", "c", "d"], 2);
```

### Explanation:

##### Steps: 

###### First: 
```javascript
//Set an empty array to put in the array groups.
var arrReturn = [];

//Create a numeric variable called (next). --To use later--.
var next = 0;
```

###### Second: 
```javascript
//Use a loop (for) to iterate through the array elements, (arr).
for(var i = 0; i < arr.length; i++){
```

###### Third: 
```javascript
//If (next) has a value of 0 it means that is the first turn of the loop.
if(next === 0 || i === next){
 //From the current index (i). 
 //The total number of elements that should be in each sub-array (that is the value of the argument (size)), is copied into the sub-array.
  
  //example:
  //arr = ["a", "b", "c", "d"];
  //size = 2;
  //i = 0;
  //arrReturn.push(sub-array = ["a", "b"]);
  arrReturn.push(arr.slice(i, i+size));
  
  //The variable named (next), as its name says.
  //Represents the next index (i). Where the previous action will be repeated until the end of the loop.
  next = i+size;
```
###### Fourth: 
```javascript
//In this example this function returns.
[["a", "b"], ["c", "d"]]
```
