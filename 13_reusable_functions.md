# 1.3 reusable functions

####Learning Goals
By the end of the lesson, students will be able to
* read and write functions

####Explore
We have created many functions for the little steps our robots need to take in order to complete the mazes. How can we sequence the functions to have robot move around the rectangle maze?

####Explain
We have created mini steps for our robots to complete the bigger maze. Let's combine some of our functions to create more effective functions.
 
1. To begin, let's create a function to move forward until robot sees the wall, turns right, and then tags the light on the right wall. 
2. Create a function and name it to describe its goal.
```js
function hitRightLight() {
  
}
```

3. Sequence the series of instructions this new function must follow to achieve its goal.
```js
function hitRightLight() {
  forwardUntilDistance()
  right()
  forward()
}
```

####Engage
1. Students may continue to create functions for actions they see repeated throughout the maze.

####Justify
Ask students to walk you through the new functions they have created. 
