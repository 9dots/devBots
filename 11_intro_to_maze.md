# Intro to maze

#### Overview
In this lesson, students will use ev3.sh to program their Lego EV3 robots to complete a series of mazes.

#### Learning Goals
By the end of the lesson, students will be able to
* read a function
* identify parameters to steer robot
* create a function
* read simple conditionals

#### Introduce Concept

##### Functions
Students will learn to create new functions to simplify their code. To begin, students will see the following code on the homepage of ev3.sh:

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

1. The first few lines of code set up ev3.sh.
2. The main function sets up the interactive page on the right side of the screen. Students may call functions in the ev3 input box to move robot.
3. A function is a reusable set of instructions. The functions in ev3.sh are written like this:
```js
function forward () {
      out('moving forward')
      steer.rotations(1, 40, 0)
      out('done')
}
```

4. 'out' displays its message on the right side of the screen when the function is called.
5. steer.rotations accepts three parameters to control the robot's movements.
  + The first parameter determines wheel rotation. 1 = one wheel rotation.
  + Second parameter determines speed. Speed can be any number between 1 - 100.
  + Third parameter determines direction. 0 is straight. A number between -100 and -1 controls severity of left turn. A number between 1 and 100 controls severity of right turn.  
  + **The forward function in the starter code moves one wheel rotation, at a speed of 40, in the straight direction.**  
6. Have students walk through back function and explain the steer.rotations parameters.
7. Create left and right functions with students and emphasize importance of correct syntax.
```js
function right() {
      out('turning right')
      steer.rotations(1, 40, 50)
      out('done')
}
function left() {
      out('turning left')
      steer.rotations(-1, 40, 50)
      out('done')
}
```

8. Any changes must be saved by pushing the ```Run Code``` button.


To take a deep dive into functions, see 'defining functions' lesson.

##### If/else Conditionals
Students will use if/else conditionals in their code to program specific instructions.

1. The main function contains a series of if/else if statements to check user input and calls a function based on the input.
```js
function main (input) {
    if (input === 'forward') {
        forward()
    } else if (input === 'back') {
        back()
    }
}
```

2. The main function sets up the interactive page on the right side of the screen. Students may call functions in the ev3 input box to move robot.
3. The main function accepts one parameter: an input from the user.
4. If the input is equal to 'forward', the ```forward()``` function is called.
5. Else, the function continues to check if the input is equal to 'back'. If that condition is true, the ```back()``` function is called.
6. Work with students to add 'else if' statements to the main function and check input for 'left' and 'right'. If true, the respective functions should be called.
7. Emphasize importance of correct syntax.

To take a deep dive into conditionals, see 'if/else conditionals' lesson.

#### Engage
1. Allow students time to create and adjust their left and right functions.
2. Have students complete a simple maze utilizing the functions they have created.
3. At the end of the day, students should save gist and name their sumo code.  

#### Questions
1. How can we further simplify your code?
2. What would make maze solving easier?
  + We can create umbrella functions that complete multiple steps of the maze. We can also utilize sensors to detect walls and know exactly when to turn.
