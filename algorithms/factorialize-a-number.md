# Factorialize a Number

### Challenge:

	* Return the factorial of the provided integer.
	* If the integer is represented with the letter n.
	* A factorial is the product of all positive integers less than or equal to n.
	* Factorials are often represented with the shorthand notation n!.
	* For example: 5! = 1 * 2 * 3 * 4 * 5 = 120
	* Remember to use 'Read Search Ask' if you get stuck. Write your own code.

### Helpful links:

  1 . [Arithmetic Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators)
  
  2 . [ReadSearchAsk](https://github.com/FreeCodeCamp/freecodecamp/wiki/FreeCodeCamp-Get-Help)
    
### Initial code:

```javascript
function factorialize(num) {
  return num;
}

factorialize(5);
```

### My solution:

[Live Example](https://jsfiddle.net/fininhop/8ghLc06j/1/)

```javascript
function factorialize(num) {
  var factor = 0;
  
  if(num === 0){
    factor = 1;
  
  }else{
    for(var i = 0; i < num; i++){

      if(factor === 0 )
        factor = i*(i+1);
      else
        factor = factor*(i+1);
      
    }
  }
  return factor;
}

factorialize(5);
```

### Explanation:

##### Steps:

###### First:
```javascript
//Set a variable named (factor) with an initial value of zero.

var factor = 0;
```

###### Second:
```javascript
//If the target (num) is zero. Set the variable (factor) to one. And return it.

if(num === 0){
  factor = 1;
```

###### Third:
```javascript
//Start a loop (for): It starts at zero and ends when the target (num) value is reached.
//Assigning the rising value of each iteration to the variable named (i).

for(var i = 0; i < num; i++){
```

###### Fourth:
```javascript
//Now, if the variable (factor) is zero.
//This means it is the first trun of the loop.

if(factor === 0 )
```

###### Fifth:
```javascript
//The variable (factor) is product of two numbers. Therefore:

//The first number (i), is one. 
//The second number is the result of the expresion (i+1). Which it is equal to two.  
//The variable (factor) , is the product of both.

factor = i*(i+1);
```

###### Sixth:
```javascript
//The following turns of that loop, do the same. 
//But as the first number. 
//Here is used the variable (factor). Previously created in the first turn of the loop.
//Unlike the variable (i).

//For example if it is the turn two of the loop.
//first trun >> factor = 1*(1+1) = 2;
//       now >> factor = 2*(2+1) = 6; 

else{
  factor = factor*(i+1);
```

###### Seventh:
```javascript
//This function returns in this example.
120
```
