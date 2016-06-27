# Truncate a string

### Challenge:

	* Truncate a string (first argument) if it is longer than the given maximum string length (second argument).
	* Return the truncated string with a ... ending.
	* Note that inserting the three dots to the end will add to the string length.
	* However, if the given maximum string length num is less than or equal to 3, then the addition of the three dots does not add to the string length in determining the truncated string.
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [String.prototype.slice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/slice)
  
  2 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)

### Initial code:

```javascript
function truncateString(str, num) {
  // Clear out that junk in your trunk
  return str;
}

truncateString("A-tisket a-tasket A green and yellow basket", 11);
```

### My solution:

[Live example](https://jsfiddle.net/fininhop/9xwL0ys2/)

```javascript
function truncateString(str, num) { 
  
  if(str.length === 3){
    return str.slice(0, -str.length+1)+'...';
  
  }else if(num < 3){
    return str.slice(0, -str.length+(num))+'...';
    
  }else if(num < str.length){
    return str.slice(0, -str.length+(num-3))+'...';
    
  }else{
    return str;
  }
  
}

truncateString("A-tisket a-tasket A green and yellow basket", 11);
```

### Explanation:

##### Steps: 

###### First: 
```javascript
//If the argument (str) has a length of three characters.
if(str.length === 3){
  
  //example:
  //-3+1 = -2
  //So str.slice(0, -str.length+1)+'...' is the same as: str.slice(0, -2)+'...';
  //The String.prototype.slice() has two arguments.
  //The first (0), is where it starts.
  //The second (-str.length+1) is the number of characters that will be recursively removed from the argument (str).
  
  return str.slice(0, -str.length+1)+'...';
```

###### Second: 

```javascript
//If the argument (num) has a value less than (3).
}else if(num < 3){
  //Assuming that:
  // str = "abcdef";
  // 1 - The argument (str) has as character length value (6). 
  // 2 - The argument (num) has as value (2).
  
  //example:
  //str.slice(0, -6+2)+'...';
  //So (-6+2) = -4.
  
  //Therefore, (-4) characters will be removed recursively of the argument (str).
  //Giving back: "ab...";
  
  return str.slice(0, -str.length+num)+'...';
```

###### Third: 
```javascript
//If the argument (num) is smaller than the length of the argument (str).
}else if(num < str.length){
  //Assuming that:
  // str = "A-tisket a-tasket A green and yellow basket";
  // 1 - The argument (str) has as character length value (43). 
  // 2 - The argument (num) has as value (11).

  //example:
  //str.slice(0, -43+(11-3))+'...';
  //So (-43+8) = -35.

  //Therefore, (-35) characters will be removed recursively of the argument (str).
  //Giving back: "A-tisket...";
  
  return str.slice(0, -str.length+(num-3))+'...';
```
