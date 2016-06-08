# intro to sensors

####Overview
Students will learn to incorporate sensors onto their sumo robots. 

####Learning Goals
By the end of the lesson, students will be able to
* write conditionals
* identify ultrasonic sensor
* identify color sensor
* write code utilizing sensors

####Introduce Concept

#####Ultrasonic Sensor
Ask students: How do we keep from walking into tables and walls?

1. We have eyes to see where we're going and what's in front of us, but robots do not.
2. However, we can attach sensors to robots to give them more abilities.
3. An ultrasonic sensor acts as the eyes of the robot, and can tell if there is an object in front. 
4. To begin, we need to set a variable named devices to the ```read()``` function. This allows us to simply use the word devices when we need to call upon a sensor. 
```js
var devices = read()
```
5. The ultrasonic sensor will be used within an if/else condition.
```js
if (devices.sonic(1) <= 24) {
  steer.forever(100, 0)
}
```
6. The sensor can be called using the command ```devices.sonic()```.
  + Within the parentheses, note the port number that the sensor is plugged into.
7. If the ultrasonic sensor sees an object less than 24 inches away, it should charge toward it.
  + In this case, students may use a steer.forever in place of steer.rotations to have the robot charge forward as much as necessary to beat its opponent. 
8. Note that the inches 



Avoid function
spin until you see monster, then move back

#####Color Sensor
Ask students: What type of sensor would help the robot stay within the lines of the sumo mat?

