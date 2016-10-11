# parameters

#### Learning Goals
Students will learn to identify and pass parameters to give computers extra information in function calls.

#### Explore
Create maze with blocks.

1. Have students complete maze with their robots using ```forward()```, ```right()```, and ```left()``` functions.
  + ```forward()``` function should be set on 1 wheel rotation

#### Questions
  + How many lines of code have you written?
  + Were there any steps that got repeated?
  + What information can we give the forward function to complete the maze more efficiently?


#### Explain
1. Sometimes functions require extra information in order to carry out its instructions. This extra information can be temporarily stored
2. Parameters are variables that only exist inside of the function.
3. Parameters are written within the parentheses of a function.
4. In ev3 shell, the parameters have the value of whatever is entered in the input box.
  + The value entered gets stored in the parameter, and is then used within the function.
5. **Ask students:** What extra information can we provide the robot to control its movement?
6. We can use parameters to control the number of wheel rotations in our functions.
  + Let's use the abbreviation ```rot``` for rotations.
```js
function forward (rot) {
        out('moving forward')
        steer.rotations(rot, 40, 0)
        out('done')
}
```

7. Now we can call functions in the input box and additionally write a number to control the number of wheel rotations.
  + Example: "forward 3"

#### Engage
1. Students will include parameters into their functions to control wheel rotations.


#### Justify
Walk through the new code and ask students to explain how the parameter gets saved and is used within the function.
