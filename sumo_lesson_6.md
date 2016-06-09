# color sensor

####Learning Goals
By the end of the lesson, students will be able to
* read and write conditionals
* identify color sensor

####Explore
Ask students: How can we help the robot from constantly falling off the sumo mat? What type of sensor can we utilize?
  + Color sensor to help robot detect color of tape on the mat.

####Explain
Have students open sumo code.

1. A color sensor is used to detect what colors are in front of it. 
2. Each color has a value assigned to it.  

| 0:0 | 1:0 |
| -- | -- |
| 0:2 | 1:2 |


| Value     | Color     |  
| ------- | --------- |  
| 0         | none      |  
| 1         | black     |  
| 2         | blue      |  
| 3         | green     |  
| 4         | yellow    |  
| 5         | red       |  
| 6         | white     |  
| 7         | brown     |  

3. To begin, we need to set a variable named devices to equal the ```read()``` function. This allows us to simply use the word devices when we need to call upon a sensor. 
```js
var devices = read()
```

4. The color sensor will be used within an if/else condition.
```js
if (devices.color(2) === 5) {
  steer.rotations(1, 40, 0)
}
```

5. The sensor is called using the command ```devices.color(2)```.
  + Within the parentheses, note the port number that the sensor is plugged into.
6. If the color sensor detects a value equal to 5 (red), it can be given a command to react.
  + In the sample, the robot will move forward one wheel rotation at a speed of 40. 
7. Color sensor uses three equal signs to check for a value. One equal sign sets a value (think of variables).
8. As a group, decide where to include the color sensor condition within the attack function.
  + Should the robot detect the color sensor first, then use the ultrasonic sensor to find its opponent? Or should the robot find its opponent, and meanwhile check for the color sensor?
```js
if (devices.sonic(1) <= 240) {
  steer.forever(100, 0)
} else if (devices.color === 5) {
  steer.rotations(-1, 100, 0)
} else {
  steer.forever(30, 70)
}
```

8. If a sensor is not working, students should check their code for the correct port number, and correct usage of equal signs.


####Engage
1. Students will program their robot to run away from a monster, but stay within the perimeter of the sumo mat. 
2. Specifications: If a monster is less than 24 inches away, robot should back away. Else if it senses the red tape, robot should move forward. Else, robot should spin in circle until it detects an object.  

####Justify
Have students walk you through their code and explain the importance of each value and condition.

