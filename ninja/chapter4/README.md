#Chapter 4

1. Create a recursive function that will calculate the fibonacci value of a number. 

    Example: 
    ```javascript
function fb(value){
	if(value<=  2){
		return 1;
	}else{
		return fb(value-1) + fb(value-2);
	}
}
console.log(fb(9));
    ```
    Use of recursion. 

2. Create a function that will recursively go through all of the elements of an array of numbers and add them. 

    Example: 
    ```javascript
	var arr = [ 1, 3, 5, 7]; 
	var sum = addRec (arr); // 16 
	function addRec(arr){
		return arr.length>1 ? arr.pop() + addRec(arr):arr[0];
	}
	console.log(sum);
    ```
    Use of recursion. 

3. Create a custom object type that will hold a number value.  

    a. Make sure that no other data type can be assigned to that variable.  
    
    b. It must hold ONLY numbers.  
    
    Validation, setters & getters, private variables 
    ```javascript
    function getter(num){
	var x = num;
	return x;
}
function setter(num){
	if(isNaN(num)){
		console.log('this is not a number');
		return;
	}else{
		return getter(num);
	}
}
console.log(setter(1));

    
    ```

4. Write a function that will accept any number of arguments and print out their data type. 

    Example: 
    ```javascript
 function test(obj){
	var value = {}.toString.call(obj).split(' ')[1].slice(0, -1).toLowerCase();
	return console.log(value);
}
function typeOf (value) {
	for(var i = 0; i < ataType.length; i++){
		test(ataType[i]);
	}
}

var ataType = [1, 6.2831, 'pi*2', [function(){}, 1], {}, function () {}];
console.log(typeOf(ataType));

     
    ```
    
    Variable argument functions & data types 

5. Write a function that will calculate the distance between two points. The function should be able to handle 2D and 3D points. 

    Example: 
    ```javascript
    function distance(x1, x2, y1, y2, z1, z2){
	if((x1===null)||((x2===null))||((y1===null))||((y2===null))){
	   return console.log('One or more of the values were not numbers');
	}
	if(isNaN(x1)||(isNaN(x2))||(isNaN(y1))||(isNaN(y2))){	
		return console.log('One or more of the values were null');
	}
	if((z1===null) ||(z2===null)){
	    return Math.sqrt(Math.pow((x1-x2),2) + Math.pow((y1-y2),2));
	}   
	return Math.sqrt(Math.pow((x1-x2),2) + Math.pow((y1-y2),2) + Math.pow((z1-z2),2));
}
console.log(distance(1, 2, 2, 2, 1, 4));

    ```
    Function overloading and validation

6. Make the function from exercise 5 accept its parameters as either a parameter list or as two arrays containing 2D or 3D point data.  

    Example: 
    ```javascript
    /* Make the function from exercise 5 accept its parameters as either a parameter list or as two arrays containing 2D or 3D point data.
Example:
distance (1, 2, 2, 2); // returns 1 (done as part of exercise 5) distance ([1,2], [2,2]); // returns 1 
distance ([1,2], [2,2,4]); // error: incompatible point data 
*/
function distance(x1, x2, y1, y2){
	if((x1===null)||((x2===null))||((y1===null))||((y2===null))){
	   return console.log('One or more of the values were not numbers');
	}
	if(isNaN(x1)||(isNaN(x2))||(isNaN(y1))||(isNaN(y2))){   
	 return console.log('One or more of the values were null');
	}
	return Math.sqrt(Math.pow((x1-x2),2) + Math.pow((y1-y2),2));
}
console.log(distance(1, 2, 2, 2));
    ```
    
    Function overloading and validation 