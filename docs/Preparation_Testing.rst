Preparation Testing
============

The testing of the robot is composed of 4 parts: Integration Test, Hardware Test, Software Test and Integration Test. This section would conclude the results of the 3 preparation test, which could concclude the behavior of the sensors.

If you are interested in the implementation of the robot, please consult `Code Base`_ to get more information.

.. _Code Base: https://github.com/haoweiqiu/Thomas-The-EV3-Engine


Ultrasonic Sensor Characterization 
-----------------

Goal: Test the capabilities and constraints of the ultrasonic sensor.

Procedure:

- The robot is placed at a specific distance away from the wall.
- The ultrasonic sensor testing program is run.
- The value shown on the EV3 block LED screen is recorded.
- Change the direction of the robot, record the angle and the distance displayed.
- Change the distance away from the wall, repeat the previous steps.
- Calculate the error of the distance measured by the ultrasonic sensor.


Expected Result: 

- Most accurate facing head on, distance gradually becoming less accurate with increasing angle.

Test Result: 

- All angles incremented by 10 from -60 to 60 degrees were tested with the ultrasonic sensor at distance of 20cm, 30cm and 40cm from the wall. 

Conclusion:

- The robot performance generally meets the specific outcomes. The ultrasonic sensor is most accurate when facing head on, and the measured distance gradually becomes less accurate with increasing angle. Specifically, when the actual distance is 30 cm from the wall, the measurements trend follows the actual distance quite closely. This is the anticipated result, as the sensor has a more accurate operating range when it is between 20-50cm from the wall. It is important to mention that since random error with ultrasonic sensor might exist at different angles due to the cone shape of its ultrasonic sensory region, which may affect the result, and may not be entirely accurate.

Action: 

- The sensors will be used to detect and avoid obstacles from 30cm away from the wall, as that is the distance where the sensor is most accurate. Further tests need to be performed for verifying the accuracy of the ultrasonic sensor.  


Ultrasonic Sensor Characterization Supplementary 
-----------------

Goal: Provide the supplementary test to test the accuracy of the ultrasonic sensor. 

Procedure:

- The robot is placed away from the wall.
- The ultrasonic sensor testing program is run. 
- The robot moves and stops at a pre-set distance from the wall.
- The value shown on the EV3 block LED screen is recorded.
- The actual distance from the wall is measured.
- Repeat previous steps 10 times


Expected Result: 

- The ultrasonic sensor is more accurate when the sensor is placed closer to the wall.

Conclusion: 

- The robot performance generally meets the specific outcomes. When robot was set to stop at distance of 20 cm, the error mean was found to be 18.14%. When robot was set to stop at distance of 30 cm, the error mean was found to be 21.03%. When robot was set to stop at distance of 40 cm, the error mean was found to be 20.14%. The trend follows the expected result. However, it is important to mention that with the error mean result, the sensor accuracy was not found to be at the desired level: it is desired to have an error mean result of 5% or less. When considering the error standard deviation result, the precision of the sensor is found to be within the acceptable error mean. 

Action: 

- In order to raise the accuracy, one action that needs to be done by the software development team might be add an offset to the ultrasonic sensor reading to cover the sensor error. Another action that needs to be done by the hardware development team might be change the ultrasonic sensor. 


Color Sensor Characterization 
-----------------

Goal: Test the accuracy of the rising edge localization with different orientation.

Procedure:

- Place the red color card over the ground. 
- Run the color sensor testing program.
- Place the color sensor at a specific distance from the color card.
- The RGB value shown on the EV3 block LED screen is recorded.
- Repeat the test for 10 times. 
- Change the distance from the color card and repeat previous steps. 


Expected Result: 

- The color sensor is more accurate when the sensor is placed closer to the ground. 

Conclusion: 

- The robot performance generally meets the specific outcomes. Since the color to be tested is red, therefore the red component should be close to value of 255 while value of green and blue should be close to 0. From the test, it can be seen that the value of red, green, and blue all decrease when the sensor to color card (ground) distance increases. When the sensor is closer to the color board, the red component is more accurate and therefore the color sensor should be placed as close to the ground as possible. Also, in terms of the red composition measured, distance at 15 mm was found to have the smallest standard deviation, and therefore the highest precision. In terms of the green composition measured, a distance of 15 mm was found to have the smallest standard deviation and therefore the highest precision. In terms of the blue composition measured, a distance of 10 mm was found to have the smallest standard deviation, and therefore the highest precision.

Action: 

- For hardware design, the color sensor should be placed as close to the ground as possible to raise accuracy and precision. Since the preparation tests for the project are over, the hardware and software design should proceed based on test results from the preparation tests. 
