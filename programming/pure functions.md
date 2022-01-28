# what are pure functions
1. Pure functions always have to return the same output for the same input
2. They are not allowed to modify the global state or outputting something
3. They only result in a return value

``` ad-example
There are probably a lot of pure function you already used like: 
- strlen()
- pow()
- sqrt()
- rand()
- time()
```

Example of a pure function:

``` javascript
function add(y,x) {
	return y + x;
}
```

Example of a non pure function:
``` javascript
var a = 5;
function badAdd(y, x){
	a = y + x;
}
```
This function is modifying the global state. 
**Bad !!!!!!!!!**

``` ad-note
Sometimes it is hard to tell if a function is  pure; However, the rule of thumb is that pure functions are like a lookup table

Example:

| key          | value  |
|--------------|--------|
| "Hi" 		   | 	2   |
| "GOTO"       | 	4   |
| "Copenhagen" | 	10  |

If the result of your functions looks like that then it's a pure function 
```