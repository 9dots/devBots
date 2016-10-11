# ultrasonic sensor

#### Learning Goals
By the end of lesson, students will be able to
* read and write conditionals
* identify ultrasonic sensor

#### Explore
Ask students: How do we keep from walking into tables and walls?
  + We have eyes to see where we're going and what's in front of us, but robots do not.
  + We can attach sensors to robots to give them more abilities.

#### Explain
Have students open sumo code.

1. An ultrasonic sensor acts as the eyes of the robot, and can tell if there is an object in front.
2. To begin, we create a function that will utilize the ultrasonic sensor.
  + Ask students to think about the main goal of this function before naming it. Will it attack, find, or run away from its opponent?
```js
function attack () {

}
```

3. Create a ```while(true)``` loop inside the function. This will ensure that the code is running as long as one of the conditions is true.
```js
function attack () {
  while(true) {

  }
}
```

4. Set a variable named sensor to the ```read()``` function. This allows us to simply use the word sensor when we need to call upon a sensor.
```js
function attack () {
  while(true) {
    var sensor = read()
  }
}
```

5. The ultrasonic sensor will be used within an if/else condition.
```js
function attack () {
  while(true) {
    var sensor = read()
    if (sensor.sonic(1) <= 240) {
      steer.forever(100, 0)
    }
  }
}
```

6. The sensor is called using the command ```sensor.sonic()```.
  + Within the parentheses, note the port number that the sensor is plugged into.
7. If the ultrasonic sensor sees an object less than 24 inches away, it should charge toward it.
  + In this case, students may use a steer.forever in place of steer.rotations to have the robot charge forward as much as necessary to beat its opponent.
  + Distance is read in milliliters, so please add a '0' at the end of number of inches.
8. If the robot is not locating another object and charging forward, what else should it do?
  + Robot can spin until it sees another object.
9. As a group, add an else statement.
```js
function attack () {
  while(true) {
    var sensor = read()
    if (sensor.sonic(1) <= 240) {
        steer.forever(100, 0)
    } else if (color === 5) {
        steer.rotations(-1, 100, 0)
    } else {
        steer.forever(30, 70)
    }
  }
}
```

8. If a sensor is not working, students should check their code for the correct port number, and correct usage of equal signs.


#### Engage
1. Students will program their robot to run away from a monster.
2. Specifications: If a monster is less than 24 inches away, robot should back away. Else, robot should spin in circle until it detects an object.  

#### Justify
Ask students to walk you through their ultrasonic code and explain each portion of the syntax.
