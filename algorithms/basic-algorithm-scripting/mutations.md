# Mutations

### Challenge:

	* Return true if the string in the first element of the array contains all of the letters of the string in the second element of the array.
	* For example, ["hello", "Hello"], should return true because all of the letters in the second string are present in the first, ignoring case.
	* The arguments ["hello", "hey"] should return false because the string "hello" does not contain a "y".
	* Lastly, ["Alien", "line"], should return true because all of the letters in "line" are present in "Alien".
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [String.prototype.indexOf()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf)
  
  2 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)

### I add:

  1 . [String.prototype.toLowerCase()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase)

  2 . [String.prototype.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)

### Initial code:

```javascript
function mutation(arr) {
  return arr;
}

mutation(["hello", "hey"]);
```

### My solution:

[Live example](https://jsfiddle.net/fininhop/x11njxq7/)

```javascript
function mutation(arr) {
  var firstStr = arr[0].toLowerCase();
  var arrSeccondStr = arr[1].toLowerCase().split('');
  var booleanResult = false;
    
  for(var i = 0; i < arrSeccondStr.length; i++){
    
    if(firstStr.indexOf(arrSeccondStr[i]) === -1)
      return false;
      
    else
      booleanResult = true;
  }
  
  return booleanResult;
}

mutation(["hello", "hey"]);
```

### Explanation:

##### Steps:

###### First:
```javascript
//The argument (arr) have two strings of characters.
//The first thing is: 
// - Convert both into lowercase, using the String.prototype.toLowerCase() method.
// - Use the String.prototype.split() method, to create an array with the characters of the second element of the argument (arr) (arr[1]).
var firstStr = arr[0].toLowerCase();
 var arrSeccondStr = arr[1].toLowerCase().split('');
  
//The second is: Create a boolean variable, whose the initial value is (false).
var booleanResult = false;
```

###### Second:
```javascript
//Iterate through the elements of the array created from the characters of the second string of the argument (arr).
for(var i = 0; i < arrSeccondStr.length; i++){

  //The String.prototype.indexOf() method, returns (-1), if the index searched is not found.
  //This function returns immediately (false), if the current letter (arrSeccondStr[i]) does not exist in the first word.
  if(firstStr.indexOf(arrSeccondStr[i]) === -1)
    return false;
  
  //Otherwise: Updating the value of the variable (booleanResult) as true.
  else
    booleanResult = true;  
```

###### Third:
```javascript
//If it comes this far, it is because all the letters of the second word were in the first. Then this function returns (true).
//OBS - In this example, this function returns: (false)
 return booleanResult;
```
