# try...catch

The try block must be followed by either exactly one catch block or one finally block (or one of both). When an exception occurs in the try block, the exception is placed in e and the catch block is executed. The optional finally block executes unconditionally after try/catch.

### Example-1 (try)

```javascript
function callMe()
{
	var a = 99;
	try {
		alert("Value of variable a is - " + a );
	} 
	catch (e) {
		alert("Error: " + e );
	}
}
callMe();
// Output: 
// Value of variable a is - 99
```

### Example-2 (try..finally)
You can use finally block which will always execute unconditionally after the try/catch. 

```javascript
function callMe()
{
	var a = 99;
	try {
		alert("Value of variable a is - " + a );
	} 

	catch (e) {
		alert("Error: " + e );
	}
	finally {
        alert("Finally block will always execute!" );
	}
}
callMe();
// Output: 
// Value of variable a is - 99
// Finally block will always execute!
```

### Example-3 (try..catch..finally)

##### throw Statement

```javascript
function callMe()
{
	var a = 99/0;
	try {
		alert("Value of variable a is - " + a );
		if(a == Infinity) {
			throw("Divided by zero");
        }
	} 

	catch (e) {
		alert("Error: " + e );
	}
	finally {
        alert("Finally block will always execute!" );
	}
}
callMe();
// Output
// Value of variable a is - Infinity
// Error: Divided by zero
// Finally block will always execute!
```
