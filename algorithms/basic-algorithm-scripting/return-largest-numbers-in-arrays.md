# Return Largest Numbers in Arrays

### Challenge:

	* Return an array consisting of the largest number from each provided sub-array.
	* For simplicity, the provided array will contain exactly 4 sub-arrays.
	* Remember, you can iterate through an array with a simple for loop, and access each member with array syntax arr[i].
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [Comparison Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators)
  
  2 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)
  
  
### Initial code:

```javascript
function largestOfFour(arr) {
  // You can do this!
  return arr;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```

### My solution:

[Live example](https://jsfiddle.net/fininhop/vfynbtpL/)

```javascript
function largestOfFour(arr) {
  var arrReturn = [];
  var bigger;
  
  for(var i = 0; i < arr[0].length; i++){
    bigger = arr[i][0];
    
    for(var y = 0; y < arr[i].length; y++){  
      if(arr[i][y] >= bigger){
        bigger = arr[i][y];
        arrReturn[i] = arr[i][y];
      }
    }
  }
  
  return arrReturn;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```

### Explanation:

##### Steps: 

###### First: 
```javascript

//Declare two variables.

//An empty array.
var arrReturn = [];

//A variable to store the highest value of each array.
var bigger;

```

###### Second:
_I use two loops. One inside the other._

* 1 Loop: Collect each element in the array.

###### Example.:
```javascript
/*

arr = [[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]

arr[0] = [
  element 1 = [4, 5, 1, 3]
  element 2 = [13, 27, 18, 26]
  etc...

So, if [i] is equals to [0].
arr[0][i] is the same as: arr[0][element 1] = [4, 5, 1, 3]

OBS - [i] actually has a numerical value. Starts at 0 and increases its value by one for each iteration.

*/

for(var i = 0; i < arr[0].length; i++){
  bigger = arr[i][0];
```

* 2nd Loop: Collect each element present in the sub-array.

###### Example.:

```javascript
/*

Supposing that: 
* - [i] and [y] are equals [0]

arr = [[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]

So: arr[0][i] = [4, 5, 1, 3];
Is the same as:
arr[0][0] = [
  0 = 4,
  1 = 5,
  2 = 1,
  etc...

Following this logic: arr[0][i][y] = 4
Is the same as: arr[0][0][0] = 4

*/

for(var i = 0; i < arr[0].length; i++){
  bigger = arr[i][0];
  
  for(var y = 0; y < arr[i].length; y++){  
```

###### Third:

```javascript
for(var i = 0; i < arr[0].length; i++){
  
  //Define the variable called bigger. With the value of the first number of the sub-array.
  bigger = arr[i][0];
```

###### Fourth:
```javascript
//For each element in the subarray.
for(var y = 0; y < arr[i].length; y++){

    //If the current item has a higher number than the value of the variable called (bigger).
    if(arr[i][y] >= bigger){
    
      //Set this value as the bigger one.
      bigger = arr[i][y];
      
      //Update with this new value, the array will be returned.
      arrReturn[i] = arr[i][y];
    }
  }
```

###### Fifth:
```javascript
//The function returns as value. A new array that contains only the highest number of each sub-array.

//So as a result, from:
largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);

//We get an array like this.
[5, 27, 39, 1001]
```
