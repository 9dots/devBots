# 1.2 ultrasonic sensor

1. An ultrasonic sensor acts as the eyes of the robot, and can tell if there is an object in front. 
2. To begin, we need to set a variable named devices to the ```read()``` function. This allows us to simply use the word devices when we need to call upon a sensor. 
```js
var devices = read()
```

3. The ultrasonic sensor will be used within an if/else condition.
```js
if (devices.sonic(1) <= 5) {
  steer.stop()
}
```

4. The sensor is called using the command ```devices.sonic()```.
  + Within the parentheses, note the port number that the sensor is plugged into.
5. If the ultrasonic sensor sees an object less than 5 inches away, it should stop.
  + In this case, students may use a steer.stop in place of steer.rotations to have the robot fully stop. 
6. If the robot is stopped in front of a wall, what can it do next?
  + Robot can turn left or right.
