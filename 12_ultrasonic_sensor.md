# 1.2 ultrasonic sensor

####Learning Goals
By the end of the lesson, students will be able to
* read and write conditionals
* identify ultrasonic sensor

####Explore
Ask students: How do we keep from walking into tables and walls?
  + We have eyes to see where we're going and what's in front of us, but robots do not.
  + We can attach sensors to robots to give them more abilities.

####Explain
Have students open maze code.

1. An ultrasonic sensor acts as the eyes of the robot, and can tell if there is an object in front. 
2. To begin, we need to set a variable named devices to the ```read()``` function. This allows us to simply use the word devices when we need to call upon a sensor. 
```js
var devices = read()
```

3. Now let's create a function to have the robot move forward until it sees a wall, and then turn right.
```js
function turnRight() {

}
```

4. The ultrasonic sensor will be used within an if/else condition.
```js
function turnRight() {
  if (devices.sonic(1) <= 5) {
    steer.stop()
  }
}
```

5. The sensor is called using the command ```devices.sonic()```.
  + Within the parentheses, note the port number that the sensor is plugged into.
6. If the ultrasonic sensor sees an object less than 5 inches away, it should stop.
  + In this case, students may use a steer.stop in place of steer.rotations to have the robot fully stop. 
7. If the robot is stopped in front of a wall, what can it do next?
  + Robot can turn right.
8. As a group, add an else statement.
```js

function turnRight (x = 50, y = 1, z = 1) {
  forwardUntilDistance(x)
  right(y)
  forward(z)
}

function forwardUntilDistance (x) {
  while (true) {
    devices = read()
    if (devices.sonic(1) <= x) {
      steer.stop()
      break
    } else {
      steer.forever(40, 0)
    }
  }
}




steer.rotations(1, 50, 50)

```

9. If a sensor is not working, students should check their code for the correct port number, and correct usage of equal signs.


####Engage
1. Students will program their robot to run away from a monster. 
2. Specifications: If a monster is less than 24 inches away, robot should back away. Else, robot should spin in circle until it detects an object.  

####Justify
Ask students to walk you through their ultrasonic code and explain each portion of the syntax. 
