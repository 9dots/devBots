# Intro to ev3.sh

####Overview
In this lesson, students will use ev3.sh to program their Lego EV3 robots.

####Learning Goals
By the end of the lesson, students will be able to
* read a function
* identify parameters to steer robot
* create a function
* read simple conditionals

####Functions
Students will see the following code on the homepage of ev3.sh:

```
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
4. The out is a message displayed on the right side of the screen throughout the function call.
5. steer.rotations controls the wheel rotation, speed, and direction of the robot. 
--* The first parameter determines wheel rotation. 1 = one wheel rotation.
..* Second parameter determines speed. Speed can be any number between 1 - 100.
..* Third parameter determines direction. 0 is straight. A number between -100 and -1 controls severity of left turn. A number between 1 and 100 controls severity of right turn. 
6. 


Introduce students to ev3.sh
Create functions for steering (ex: forward, back, left, right)
Have students complete simple maze using the functions

lesson 6 - working on your code worksheet
lesson 7 - working on your build worksheet