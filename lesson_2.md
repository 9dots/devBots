# defining functions

####Learning Goals
Students will learn to define new functions to reuse a series of instructions.

####Explore
Students will create functions to complete a maze. The goal is to complete the maze in the fewest lines of code. 

(Create staircase maze)

1. Have students complete maze with their robots using only the forward, back, left, and right functions.

####Questions
  + How many lines of code have you written?
  + Were there any steps that got repeated?
  + What can we do to lessen the number of lines of code?


####Explain
1. Students can create functions for their repeating steps. 
2. A function is a reusable set of instructions so this will help students shorten their code.
3. To define a new function, begin with the key word ```function```. 
4. Next, name the function.
5. A function name must always be followed by open and close parentheses. 
6. Then, the function requires open and close curly braces. The instructions for the function will be written between the two curly braces.
  + Once the open curly brace is written, immediately press enter to create the closing curly brace. This will also leave a line between the two curly braces to write the instructions.
```js
function forward () {
  out('moving forward')
  steer.rotations(1, 40, 0)
  out('done')
}
```

####Engage
1. Students will create new functions to shorten their code to complete the maze.
2. Tally number of commands each student had to enter.
3. Students should save code as 'defining functions'. (This code should be separate from their sumo code). 
 
 
####Justify
Walk through the new code and ask students to explain each line and symbol used in creating a function. 
