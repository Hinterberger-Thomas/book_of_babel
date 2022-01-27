# immutability
immutability means the state is not changing. Practically speaking, immutability means that all variables are constant.

## how does it work
It is pritty simple! Instead of chaning the state of your variables you simply create a new variable.

## why everything constant
Most of the issues come from a variable which does not have the value you expected it to have; So, you have to search for the error and where the state was mutated. 

Well, what if instead mutating state is not allowed? With immutability, since every instance is const, you always know what is the value contained inside a var and where it orginated. 

### Local reasoning 
Immutability (and [[pure functions]]) unlocks local reasoning. You do not need to check the current state of the application, the global context, the current value of every variable. You can reason about a single function. All you need to know is the inputs and the output.

##