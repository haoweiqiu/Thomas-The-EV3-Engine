Hardware Testing
============

The testing of the robot is composed of 4 parts: Integration Test, Hardware Test, Software Test and Integration Test. This section would conclude the results of the 2 hardware test, which could conclude the hardware behavior of the robot design.

If you are interested in the implementation of the robot, please consult `Code Base`_ to get more information.

.. _Code Base: https://github.com/haoweiqiu/Thomas-The-EV3-Engine


Static Launcher Primary 
-----------------

Goal: Test the capabilities and constraints of the launcher.

Procedure:

- The robot is placed at fixed distance.
- The static launching testing program is run.
- Launch the ball.
- Measure the distance of the launch.
- Repeat previous test for 10 times.

Expected Result: 

- The robot is expected to launch the ball at distance of around 4.5 tiles with a relatively high precision. 

Conclusion: 

- The robot performance generally meets the specific outcomes. The mean coordinate was found to be (-8.89 cm, 143.22 cm) and the standard deviation coordinate was found to be (4.81 cm, 9.14 cm). However, the physical configuration was found not stable enough and broke down after the test. Also, based on the data, the standard deviation of the final ball launch point was found to be high and therefore the precision of the launcher might not be high enough for project delivery.

Action: 

- For the hardware development team, the launching feature of the robot is not reliable enough for the project delivery. From one aspect, the attachment of the robot should be improved, since some parts are not stable enough, which could lead to physical deterioration. From another aspect, the launch track should be improved since the current trajectory leans towards left instead of shooting the ball exactly straight forward.


Static Launcher Beta test 
-----------------

Goal: Test the capabilities and constraints of the launcher.

Procedure:

- The robot is placed at fixed distance.
- The static launching testing program is run.
- Launch the ball.
- Measure the distance of the launch.
- Repeat previous test for 10 times.


Conclusion: 

- The spring and launching mechanism has difficulties remaining attached to the motor. The distance that the ball is launched is closer to 5 tiles than before. This is in part due to an extra spring. This gave more consistent launches, but did have a tendency to break off after the 3rd or 4th launch. There was slightly less variance in the x direction and a lower tendency for the ball to launch to the left. This was likely due to the magazine being added to the launcher, putting pressure on the balls in the launcher, forcing them to tend more to the right than before.

Action: 

- More tape was added to support the spring and launch mechanism. Additional methods are being explored to keep the launcher mechanism from detaching. 


Static Launcher Improvement 
-----------------

Goal: Test the capabilities and constraints of the improved launcher after beta demo.

Procedure:

- The robot is placed at fixed distance.
- The static launching testing program is run.
- Launch the ball.
- Measure the distance of the launch.
- Repeat previous test for 10 times.


Expected Result: 

- Again, the robot is expected to launch the ball at distance of around 4.5 tiles with a relatively high precision.

Conclusion: 

- According to the analysis, the mean for x and y coordinates were found to be      -14.12 cm and 132.94 cm. The standard deviation was found to be 6.51 cm and 9.59 cm for x and y coordinates respectively. Since the standard deviations for x and y are both larger than 1 cm, the launcher is still not stable enough for the final competition. During the test, it was found that the attachment of the launcher components was still unstable to the point where the tester had to manually attach the launcher when the launcher parts were loosened. The loosening of parts of the launcher might be a great influence for the stability of the robot launching function. 
Action: 

- The hardware team should find a way to make the launcher more stable to avoid attachment loosing. 
