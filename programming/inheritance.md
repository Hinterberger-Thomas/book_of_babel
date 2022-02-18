# inheritance
Inheritance is one of the most important aspects of oop. The key takeaway of inheritance is **code re-usability**. In place of writing the same code, again and again, we can simply inherit the properties of one class into the other.
```` ad-example
title: example of inheritance
collapse: open
In this example the `SwimmingMonster` inherits all the methods and properties from the `Monster` object.
``` javascript 
class Monster{
	constructor(name){
		this.name = name;
	}
	attack(){
		console.log("${this.name} attacked")
	}
}

class SwimmingMonster extends Monster {
	swim() {
		console.log("${this.name} swam")
	}
}

```
````

## why not
**1. Inheritance unnecessary methods**
The child class needs to inherit all the properties and the methods from the parent class, even if it is not used. This creates more complexity in the child class than is needed to.
**2. in**