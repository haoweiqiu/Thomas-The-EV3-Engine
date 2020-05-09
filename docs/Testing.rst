Testing
============

The testing of the robot is composed of 3 parts: Hardware Test, Software Test and Integration Test. This section would conclude the results of the 3 integration test, which could conclude the software and hardware behavior of the robot design.

If you are interested in the implementation of the robot, please consult `Code Base`_ to get more information.

.. _Code Base: https://github.com/haoweiqiu/Thomas-The-EV3-Engine


Integration Test 1
-----------------

Goal: Test the accuracy of the rising edge localization with different orientation.

Procedure:

- The robot is placed in a tile corner along a random angle, where two walls are present.
- Select Map green 1 left in the map library. 
- Run the software program.
- Record the final location when stop and ready to launch balls. 
- Record if the ball launches and shoot into the basket. 
- Repeat the previous steps for 10 times.

Conclusion:

- For the test the location where the robot launches the ball, the mean for x coordinate was found to be 284.76 cm and the mean for y coordinate was found to be 129.84 cm. Since the standard deviation for the x coordinate was found to be 7.06 cm and for the y coordinate the standard deviation was found to be 11.98 cm, the accuracy is not enough for the final competition. From the launch result, it was found that the pass rate was only 10%, which means that the software needs to be improved immediately. 


Integration Test 2
-----------------

Goal: Test the accuracy of the rising edge localization with different orientation.

Procedure:

- The robot is placed in a tile corner along a random angle, where two walls are present.
- Run the software program.
- Record the final location when stop and ready to launch balls. 
- Record if the ball launches and shoot into the basket. 
- Repeat the previous steps for 10 times.

Conclusion:

- For the test the location where the robot launches the ball, the mean for x coordinate was found to be 277.92 cm and the mean for y coordinate was found to be 138.44 cm. Since the standard deviation for the x coordinate was found to be 7.69 cm and for the y coordinate the standard deviation was found to be 8.90 cm, even though the accuracy of the robot is improved, the accuracy is still not enough for the final competition. From the launch result, it was found that the pass rate was only 30%, which means that the software still needs to be improved immediately.


Integration Test 3
-----------------

Goal: Test the accuracy of the rising edge localization with different orientation.

Procedure:

- The robot is placed in a tile corner along a random angle, where two walls are present.
- Select Map green 1 left in the map library. 
- Run the software program.
- Record the final location when stop and ready to launch balls. 
- Record if the ball launches and shoot into the basket. 
- Repeat the previous steps for 10 times.

Conclusion:

- For the test the location where the robot launches the ball, the mean for x coordinate was found to be 278.14 cm and the mean for y coordinate was found to be 149.51 cm. Since the standard deviation for the x coordinate was found to be 7.38 cm and for the y coordinate the standard deviation was found to be 9.57 cm, even though the accuracy of the robot is improved, the accuracy is still not enough for the final competition. From the launch result, it was found that the pass rate was only 10%, which means that the software still needs to be improved immediately.
