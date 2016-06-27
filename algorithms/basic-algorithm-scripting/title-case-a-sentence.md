# Title Case a Sentence

### Challenge:

	* Return the provided string with the first letter of each word capitalized.
	* Make sure the rest of the word is in lower case.
	* For the purpose of this exercise, you should also capitalize connecting words like "the" and "of".
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [String.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)
  
  2 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)
  
### I add:

  1 . [Array.Map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

### Initial code:

```javascript
function titleCase(str) {
  return str;
}

titleCase("I'm a little tea pot");
```

### My solution:

[Live example](https://jsfiddle.net/fininhop/utjs2k1g/)

```javascript
function titleCase(str) {
  var arrWords = str.toLowerCase().split(' ');
  var arrChars;
  var i = 0;
  
  arrWords.map(function(val){

    arrChars = val.split('');
    arrChars[0] = arrChars[0].toUpperCase();
    
    arrWords[i] = arrChars.join('');
    
    i++;
  });
  
  return arrWords.join(' ');
}

titleCase("I'm a little tea pot");
```

### Explanation:

_In this challenge the use of_ 
[Array.Map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) 
_is identical to the previous one:_ 
[find-the-longest-word-in-a-string >>Third Step  ](https://github.com/fininhop/free-code-camp/blob/master/algorithms/basic-algorithm-scripting/find-the-longest-word-in-a-string.md#third)

_Somehow_
[Array.Map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) 
_is just a way to iterate through each element of an_ [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array).

_Other ways of doing the same would be using:_

[forEach()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach), [for()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for),
[while()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while)

##### Steps: 

###### First: 
```javascript
//See above explanation, this has already been explained on another challenge.
//The only difference so far is:
// * - Each character in the string is converted to lowercase.

var arrWords = str.toLowerCase().split(' ');
var arrChars;
var i = 0;

arrWords.map(function(val){
```

###### Second: 
```javascript
arrWords.map(function(val){
  
  //Divide the word in letters. Then create an array (arrChars) with the result.
  arrChars = val.split('');
  
  //Get the first letter of the current word, and transform it into capital.
  arrChars[0] = arrChars[0].toUpperCase();
  
  //By bringing together, all the items of the array called (arrayChars). Is achieved as a result: 
  //The same word as before, but with the first letter capitalized.
  //Finally, the array named (arrWords) is updated with this value.
  arrWords[i] = arrChars.join('');
  
  i++;
});    
```

###### Third: 
```javascript
//Each word stored in the array (arr). Have had their first letter capitalized.
//The return value is:
//All these words back together in the sentence.
return arrWords.join(' ');

//In this example it would be:
//I'm A Little Tea Pot
```
