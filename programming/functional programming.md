# what is functional programming (FP)
In simple terms it is nothing more than [[pure functions]] and state that is [[immutability]]; Using these two options lead to better read- and maintainability. FP is inspired by mathematical functions, which always produce the same output, giving the same input. 

## why 
- State has to be immutabile and that leads to a better understanding of state changes.
- You always know what you gonna get. [[pure functions]] always produce predictable results
- Due to the nature of [[pure functions]] code is getting split into smaller bits and is, therefore, more readable
	- Easier testing (predictable behaviour)
	- [[pure functions]] do not depend on the global state, so they only need the necessary parameters
- The separation of logic and data makes code easier to read [[object oriented programming]]
- [[Thread safety]]; due to immutable state

## Don't iterate
Iterating is pritty much out of the question because you need to mutate your vars

Instead use
- [[declarative programming]]
- [[recursion]] 

## examples
Not functional:
``` javascript
var name = name;

var greeting = "Hi, I'm "

console.log(greeting + name)
```

functional:
``` javascript
function greet(name) {
	return "Hi, I'm " + name;
}
greet('Anjana')
```

## sources 
[# Learning Functional Programming with JavaScript - Anjana Vakil - JSUnconf](https://www.youtube.com/watch?v=e-5obm1G_FY)

