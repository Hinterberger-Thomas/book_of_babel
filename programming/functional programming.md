# what is functional programming
In simple terms it is nothing more than [[pure functions]] and state that is (immutable)[immutability]; Using these two options lead to better read- and maintainability. FP is inspired by mathematical functions, which always produce the same output, giving the same input. 

## why 
Using a programming paradigm can increase the maintenance and readability; however, it can lead to less performant code. In the end, it comes down to personal preference and what is needed. High performant code is usually not the most important requirement; Code that is maintainable and features can simply be added, is far more valuable. 

## how does it work
**[[immutability]]**
- Data won't change
	- The core principle of [[immutability]] is that data won't change
	- The advantage of this would be that we are in control of the data and it won't change behind our backs (no [[side effekts]]).
- [[Thread-safety]]
	- Because of the [[immutability]] it is guaranteed that two threads won't change the obj at the same time
	- This also means you do not have to implement any functionality to provide thread safety
- Better cacheability
	- due to the saving of the previous state
**[[pure functions]]**
- They are simply to debug 
- Same input results in same output 
- They are easier to understand 
**[[Recursion]]**
