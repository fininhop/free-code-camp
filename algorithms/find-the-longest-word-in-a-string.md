# Find the Longest Word in a String 

### Challenge:

	* Return the length of the longest word in the provided sentence.
	* Your response should be a number.
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [String.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)
  
  2 . [String.length()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/length)
  
  3 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)
  
### I add:

  1 . [Array.Map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

### Initial code:

```javascript
function findLongestWord(str) {
  return str.length;
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```

### My solution:

[Live example](https://jsfiddle.net/fininhop/qe5a5s56/)

```javascript
function findLongestWord(str) {
  var arrStr = str.split(' ');
  var bigger;
  var i = 0;
  
  arrStr.map(function(val){
    i++;
    
    if(i === 1){
      bigger = val.length;  
    }else{
      if(bigger < val.length)
        bigger = val.length;
    }
  });
  
  return bigger;
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```

### Explanation:

##### Steps: 

###### First: 
```javascript
//The array called (arrStr) saves each word of the text string (str).
//By dividing the content of the phrase by blanks. "str.split('WHITE_SPACE')".
var arrStr = str.split(' ');
```

###### Second:
```javascript
//Create the variable named (bigger) to use later.
var bigger;
//Create a variable called (i) and assign zero as value.
var i = 0;
```

###### Third:

_The map() method creates a new array with the results of calling a provided function on every element in this array._

```javascript
//For each element in the array:
//It is added a round more in the loop.
//The variable (i) adds one to its own value.
//The parameter (val) contains every word in the target string (srt).
arrStr.map(function(val){
  i++;
```

###### Fourth:
```javascript
//This means it is the first round.
if(i === 1){
  //Set the variable called (bigger), with the total number of characters in the target (srt).
  bigger = val.length;  
```

###### Fifth:
```javascript
else{
//Now, the variable (bigger) has a value.
//Therefore, if the current word has more characters than the largest word above (bigger) has?
//The variable (bigger) is updated with the largest value.
if(bigger < val.length)
  bigger = val.length;
```
