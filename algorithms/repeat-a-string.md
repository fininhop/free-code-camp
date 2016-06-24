# Repeat a string

### Challenge:

	* Repeat a given string (first argument) num times (second argument). Return an empty string if num is not a positive number.
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [Global String Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
  
  2 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)

### Initial code:

```javascript
function repeatStringNumTimes(str, num) {
  // repeat after me
  return str;
}

repeatStringNumTimes("abc", 3);
```

### My solution:

[Live example](https://jsfiddle.net/fininhop/6v4ug0mt/)

```javascript
function repeatStringNumTimes(str, num) {
  var str_return = '';
  for(var i = 0; i < num; i++)
    str_return += str;

  return str_return;
}

repeatStringNumTimes("abc", 3);
```

### Explanation:

```javascript
//Create a variable to store the repeated word.
var str_return = '';

//Use a loop (for), whose the total number of truns is the argument (num).
//For each turn of the loop, another instance of the argument (str) is added into the variable (str_return).
for(var i = 0; i < num; i++)
  str_return += str;
```
