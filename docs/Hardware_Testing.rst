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

Result Analysis:

- The robot performance generally meets the specific outcomes. However, the physical configuration was found not stable enough and broke down after the test. Also, based on the data, the standard deviation of the final ball launch point was found to be high and therefore the precision of the launcher might not be high enough for project delivery.


Static Launcher Improvement 
-----------------

Goal: Test the capabilities and constraints of the improved launcher after beta demo.

Procedure:

- The robot is placed at fixed distance.
- The static launching testing program is run.
- Launch the ball.
- Measure the distance of the launch.
- Repeat previous test for 10 times.


Result Analysis:

- During the test, it was found that the attachment of the launcher components was still unstable to the point where the tester had to manually attach the launcher when the launcher parts were loosened. The loosening of parts of the launcher might be a great influence for the stability of the robot launching function. 

