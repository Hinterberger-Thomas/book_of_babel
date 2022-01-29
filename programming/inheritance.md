# inheritance
```` ad-example
title: example of inheritance
collapse: close

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