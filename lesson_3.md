# If/else Conditionals

####Learning Goals
Students learn to read and write if/else conditionals.

####Explore
Students will use if/else conditionals in their code to program specific instructions.
  
Begin by playing a game where students react to different situations based on instructions. For example:

1. Start with an if statement:
```js
if (shirtColor === 'red') {
  patHead()
} 
```
2. Add an else if and an else statement to continue giving instructions to a specific group of students.
```js
if (shirtColor === 'red') {
  patHead()
} else if (shirtColor === 'blue') {
  tapNose()
} else {
  smile()
}
```
3. Allow students to interpret the rules on their own and act based on the condition. 

####Questions
1. Why were the conditionals (if/else) important for this exercise?
2. What special syntax did you notice in the code?
3. Why do you think there are three equal signs?
4. How do you think you can use conditionals to program your sumo robot?

####Explain
1. If/else conditionals are used to give instructions to a group that meets a specific condition. 
2. In our game, only students that met the rule of wearing a red shirt or blue shirt received different instructions. 
3. Write an if/else statement for the main function with the class.
4. To write a conditional, we begin with the key word ```if```.  
```js
if
```
5. In parentheses, we write our condition.
  + What must be true or what must happen first?
```js
if (input === 'forward')
```
6. Within curly braces, we write the result of that condition. If the input is equal to forward, what must happen after?
  + We will want to call the forward function so the robot can perform that task.
  + Note the placement of the curly braces. Does this syntax look familiar?
```js
if (input === 'forward') {
  forward()
}
```
7. To continue checking for conditions, use the key words ```else if``` and write the condition and instructions. 
```js
if (input === 'forward') {
  forward()
} else if (input === 'back') {
  back()
}
```
8. To catch all others that do not meet a condition, we can use the key word ```else``` and give that group an instruction as well.






