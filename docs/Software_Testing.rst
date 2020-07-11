Software Testing
============

The testing of the robot is composed of 4 parts: Integration Test, Hardware Test, Software Test and Integration Test. This section would conclude the results of the 5 software test, which could conclude the software behavior of the robot design.

If you are interested in the implementation of the robot, please consult `Code Base`_ to get more information.

.. _Code Base: https://github.com/haoweiqiu/Thomas-The-EV3-Engine


Odometer
-----------------

Goal: Test the accuracy of the odometer program, including square driver and the accuracy of the 360 degrees turning.

Procedure:

- The robot is placed over the board
- Run the square driver testing program.
- When the robot finish moving, measure the actual location of the robot.
- Record the reading from the LED screen.
- Repeat previous steps for 10 times.


Expected Result: 

- For the square driver, the final calculated Euclidean error distance should be smaller than 5 cm, which means that the robot design is accurate enough. For the 360-degree turn, the angle error calculated should be smaller than 3 degrees, which means that the turning of the robot design is accurate enough for project delivery.

Conclusion:

- For the 360-degree turn, the error angle mean was found to be 18.10 and the error angle standard deviation was found to be 3.81, the turning is also not accurate enough. According to the data, this might be caused by the inequivalent load on left and right side of the robot, which leads to the robot tends to overturn on each turn.

Action: 

- The software team should adjust the speed of both motors and change other constant in order to fix the overturn problem. The hardware team should adjust the physical design of the robot so that the load on left and right side of the robot is similar.


Rising Edge Localization
-----------------

Goal: Test the accuracy of the rising edge localization with different orientation.

Procedure:

- The robot is placed in a tile corner along the 45-degree line, where two walls are present.
- Run the rising edge localization program.
- Note the final position and final angle of the robot.
- Compute the Euclidean distance error and final angle error.
- Repeat previous test for 10 times.


Expected Result: 

- The rising edge localization should localize the robot in high accuracy and precision to (1,1) point. 

Conclusion:

- Since the Euclidean distance error mean was found to be 0.07 cm and the final angle error mean was found to be 0 degree, the accuracy of the rising edge localization is very high and is enough for project delivery. 

Action: 

- The localization part shall be labelled as finished. The software team shall focus more on improving the accuracy of both navigation and obstacle avoidance. 


Falling Edge Localization
-----------------

Goal: Test the accuracy of the falling localization program.

Procedure:

- The robot is placed in a tile corner along the 45-degree line, where two walls are present.
- Run the falling edge localization program.
- Note the final position and final angle of the robot.
- Compute the Euclidean distance error and final angle error.
- Repeat previous test for 10 times.


Expected Result: 

- The falling edge localization should localize the robot in high accuracy and precision to (1,1) point. 

Conclusion:

- It is found that the accuracy of the rising edge localization is very high and is accurate enough for project delivery. It is also found that the rising edge is preferable for the final competition rather than falling edge localization since with the data from the previous test, the rising edge localization was found to have smaller mean and standard deviation. 

Action: 

- The error found in the beta demo was finally fixed and the localization part shall be finally labelled as finished. The software team shall focus more on implementation of the obstacle avoidance. 

Obstacle Avoidance
-----------------

Goal: Test the accuracy of the obstacle avoidance program. 

Procedure:

- Place the robot at (1,1) on the board.
- Place an obstacle in front of the robot at (1,2) on the board. 
- Run the obstacle avoidance test program. 
- Measure the final actual location of the robot.
- Calculate the error distance.
- Repeat the previous steps for another 9 trials.


Expected Result: 

- The obstacle avoidance program is expected to avoid obstacle with relative high accuracy. 

Conclusion:

- From the testing result, it was found that the error mean was 5.61 cm and the standard deviation of the error was found to be 3.30 cm. The accuracy of the obstacle avoidance is relatively high enough. 

Action: 

- The software team shall continue with implementation of localization and shall start preparation of software integration.

Localization Orientation
-----------------

Goal: Test the accuracy of the falling edge localization with different orientation.

Procedure:

- The robot is placed in a tile corner along a specific orientation angle for testing, where two walls are present.
- Run the falling edge localization program.
- Note the final position and final angle of the robot.
- Compute the Euclidean distance error and final angle error.
- Change the orientation angle by increasing 45 degrees to previous orientation, repeat the previous steps.


Expected Result: 

- The falling edge localization should be precise in all orientation angles.

Conclusion:

- From all tests conducted, it was found that the current localization works accurately when the starting orientation angle is 0, 45, 180 and 225 degrees. The result shows that the current software design might have limitation on the starting orientation. 

Action: 

- The software team should check the localization method and fix the current limitation so that the localization shall work in all starting orientation. 
