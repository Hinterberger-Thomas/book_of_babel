# what is object oriented programming (OOP)
OOP uses the concepts of [[classes]] and [[objects]]. It is being used to structure a program in to small and reusable pieces of code. Instances of [[classes]] are used to create objects. 
``` javascript
var a = new Rectangle();
```
A **class** is an like an abstract blueprint. Classes often represent things like **cars** or **animals** (just like in the real world). This class defines the attributes and the functions (the overall structure). 

```` ad-example
title: example of a js class
collapse: open

One way to define a class is using a **class declaration**. To declare a class, you use the `class` keyword with the name of the class ("Rectangle" here).


``` javascript
class Rectangle {

 constructor(height, width) {

 this.height = height;

 this.width = width;

 }

}
```
````
## why
- Reusable, OOP objects can be reused across the program
- [[encapsulation]]
- [[polymorphism]]
- [[inheritance]]
- [[abstraction]]

## why not 
