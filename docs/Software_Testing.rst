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


Result Analysis:

- For the 360-degree turn, the error angle mean was found to be 18.10 and the error angle standard deviation was found to be 3.81, the turning is also not accurate enough. According to the data, this might be caused by the inequivalent load on left and right side of the robot, which leads to the robot tends to overturn on each turn.


Rising Edge Localization
-----------------

Goal: Test the accuracy of the rising edge localization with different orientation.

Procedure:

- The robot is placed in a tile corner along the 45-degree line, where two walls are present.
- Run the rising edge localization program.
- Note the final position and final angle of the robot.
- Compute the Euclidean distance error and final angle error.
- Repeat previous test for 10 times.


Result Analysis:

- Since the Euclidean distance error mean was found to be 0.07 cm and the final angle error mean was found to be 0 degree, the accuracy of the rising edge localization is very high and is enough for project delivery. 


Falling Edge Localization
-----------------

Goal: Test the accuracy of the falling localization program.

Procedure:

- The robot is placed in a tile corner along the 45-degree line, where two walls are present.
- Run the falling edge localization program.
- Note the final position and final angle of the robot.
- Compute the Euclidean distance error and final angle error.
- Repeat previous test for 10 times.


Result Analysis:

- It is found that the accuracy of the rising edge localization is very high and is accurate enough for project delivery. It is also found that the rising edge is preferable for the final competition rather than falling edge localization since with the data from the previous test, the rising edge localization was found to have smaller mean and standard deviation. 


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

Result Analysis:

- From the testing result, it was found that the error mean was 5.61 cm and the standard deviation of the error was found to be 3.30 cm. The accuracy of the obstacle avoidance is relatively high enough. 


Localization Orientation
-----------------

Goal: Test the accuracy of the falling edge localization with different orientation.

Procedure:

- The robot is placed in a tile corner along a specific orientation angle for testing, where two walls are present.
- Run the falling edge localization program.
- Note the final position and final angle of the robot.
- Compute the Euclidean distance error and final angle error.
- Change the orientation angle by increasing 45 degrees to previous orientation, repeat the previous steps.

Result Analysis:

- From all tests conducted, it was found that the current localization works accurately when the starting orientation angle is 0, 45, 180 and 225 degrees. The result shows that the current software design might have limitation on the starting orientation. 
