# color sensor

####Learning Goals
By the end of the lesson, students will be able to
* read and write conditionals
* identify color sensor

####Engage
Ask students: How can we help the robot from constantly falling off the sumo mat? What type of sensor can we utilize?
  + Color sensor to help robot detect color of tape on the mat.

####Explain
Have students open sumo code.

1. A color sensor is used to detect what colors are in front of it. 
2. Each color has a value assigned to it.  
| Value     | Color     |  
| :-------: | --------- |  
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

3. The color sensor will be used within an if/else condition.
```js
if (devices.color(2) === 5) {
  steer.rotations(1, 40, 0)
}
```

4. The sensor is called using the command ```devices.color(2)```.
  + Within the parentheses, note the port number that the sensor is plugged into.
5. If the color sensor detects a value of 5, which is equivalent to the color red, it should move forward one wheel rotation at 40 speed.
  + In this case, students may use a steer.forever in place of steer.rotations to have the robot charge forward as much as necessary to beat its opponent. 
6. If the robot is not locating another object and charging forward, what else should it do?
  + Robot can spin until it sees another object.
7. As a group, add an else statement.
```js
if (devices.sonic(1) <= 240) {
  steer.forever(100, 0)
} else if (color === 5) {
  steer.rotations(-1, 100, 0)
} else {
  steer.forever(30, 70)
}
```

8. If a sensor is not working, students should check their code for the correct port number, and correct usage of equal signs.
9. Save gist.

####Engage
1. Students will program their robot to run away from a monster. 
2. Specifications: If a monster is less than 24 inches away, robot should back away. Else, robot should spin in circle until it detects an object.  

####Justify
Ask students to walk you through their ultrasonic code and explain each portion of the syntax. 

