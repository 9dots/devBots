# Intro to ev3.sh

####Overview
In this lesson, students will use ev3.sh to program their Lego EV3 robots.

####Learning Goals
By the end of the lesson, students will be able to
* read a function
* identify parameters to steer robot
* create a function
* read simple conditionals

####Introduce Concept

#####Functions
Students will see the following code on the homepage of ev3.sh:

```js
var {loop, move, motor, read, sleep, out} = require('robot-loop')
loop(main /*,ip address*/)

var steer = move()

function main (input) {
  if (input === 'forward') {
    forward()
  } else if (input === 'back') {
    back()
  }
}

function forward () {
  out('moving forward')
  steer.rotations(1, 40, 0)
  out('done')
}

function back () {
  out('moving back')
  steer.rotations(-1, 40, 0)
  out('done')
}
```

1. ```var steer = move()``` sets up the robot steering command.
2. The main function sets up the interactive page on the right side of the screen. Students may call functions in the ev3 input box to move robot.
3. A function is a reusable set of instructions. The functions in ev3.sh are written like this:
```
function forward () {
  out('moving forward')
  steer.rotations(1, 40, 0)
  out('done')
}
```
4. The out is a message displayed on the right side of the screen when the function is called.
5. steer.rotations controls the wheel rotation, speed, and direction of the robot. 
  + The first parameter determines wheel rotation. 1 = one wheel rotation.
  + Second parameter determines speed. Speed can be any number between 1 - 100.
  + Third parameter determines direction. 0 is straight. A number between -100 and -1 controls severity of left turn. A number between 1 and 100 controls severity of right turn. 
6. The forward function currently moves one wheel rotation, at a speed of 40, in the straight direction. 
7. Walk through back function and ask students to explain the steer.rotations parameters. 
8. Allow students to connect their robots and call the forward and back function to move their robot.
9. Any changes must be saved by pushing the ```Run Code``` button. 

#####If/else Conditionals
Students will utilize if/else if conditionals in their code to program specific instructions.

Explore 
  
Play a game where students react to different situations based on instructions. For example:



####Engage
1. As a group, work with students to create a left and right function. Discuss importance of syntax and go step by step.
2. Add else if to main function to accept input for left and right functions.
3. Have students complete a simple maze using the new functions. 




lesson 6 - working on your code worksheet
lesson 7 - working on your build worksheet