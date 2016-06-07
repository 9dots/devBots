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
  cheeseSmile()
}
```
3. Allow students to interpret the rules on their own and act based on the condition. 

####Questions
1. Why were the conditionals (if/else if) important for this exercise?
2. What special syntax did you notice in the code?
3. Why do you think there are three equal signs?
4. How do you think you can use conditionals to program your sumo robot?

####Explain
1. If/else conditionals are used to give instructions to a group that meets a specific condition. 
2. In our game, we only had instructions for students that were wearing a red shirt or blue shirt. 
3. To write a conditional, we begin with the key word ```if```. 
4. In parentheses, we write our condition.
  + What must be true or what must happen first?
5. Within curly braces, we write the result of that condition. If the shirt color is equal to red, what must happen after?
6. All other conditions follow the same format with an 'else if' before the condition. 
  7. To catch all other groups that do not meet a condition, we can use the key word ```else```.