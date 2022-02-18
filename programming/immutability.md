# immutability
immutability means the state is not changing. Practically speaking, immutability means that all variables are constant.

## how to safe state if it can't be changed
Copies, copies and much more copies. Is the most simple solution. Instead of mutating the var, you create a mutated copy of it.

Bad example, the var name is changed (immutability rule violated): 
``` javascript
name = "Leon"
name += " House"
```

No var is getting changed (immutability rule being used):
``` javascript 
firstname = "Leon"
lastname = "House"
name = "${firstname} ${lastname}"
```


#### Performance
This copy hell of course usually leads to less performant code. Instead of mutating the state, you create a whole copy, which can result in a lot of unused memory.
``` ad-example
collapse: open
Imagine a big array (~3 million values). You want to edit only the first, however, you need to copy the whole thing (pretty expensive isn't it) 

```

### Persistent Data Structures (PDS)
``` ad-note
title: PDS & javascript
collapse: open
Javascript does not have a native implementation of PDS, therefore I used the library `Immutable.js`
```
Simply spoken PDS are like git. With every change, they create a new "version" of themself. Using such structures has many benefits like performance improvements.

``` javascript
var todos = {  
⋮  
t79444dae: { title: 'Task 50001', completed: false },  
t7eaf70c3: { title: 'Task 50002', completed: false },  
t2fd2ffa0: { title: 'Task 50003', completed: false },  
t6321775c: { title: 'Task 50004', completed: false },  
**t2148bf88**: { title: 'Task 50005', completed: false },  
t9e37b9b6: { title: 'Task 50006', completed: false },  
tb5b1b6ae: { title: 'Task 50007', completed: false },  
tfe88b26d: { title: 'Task 50008', completed: false },  
⋮  
(100,000 items)  
}
```
 around 50005th elements
 
 Now we want to edit this list
 
``` javascript
var nextState = toggleTodo(todos, 't2148bf88')
```
This single operation took **134ms** to run.

``` javascript 
var todos = Immutable.fromJS({  
⋮  
t79444dae: { title: 'Task 50001', completed: false },  
t7eaf70c3: { title: 'Task 50002', completed: false },  
t2fd2ffa0: { title: 'Task 50003', completed: false },  
t6321775c: { title: 'Task 50004', completed: false },  
**t2148bf88**: { title: 'Task 50005', completed: false },  
t9e37b9b6: { title: 'Task 50006', completed: false },  
tb5b1b6ae: { title: 'Task 50007', completed: false },  
tfe88b26d: { title: 'Task 50008', completed: false },  
⋮  
(100,000 items)  
})
```
Having represented our data using an `Immutable.Map`, let’s update it.

``` javascript 
var nextState = toggleTodo(todos, 't2148bf88')
```
This operation takes only **1.2 ms** to run. More than 100x faster!

[took my infos](https://medium.com/@dtinth/immutable-js-persistent-data-structures-and-structural-sharing-6d163fbd73d2)

