System
============

The System report is composed of 2 parts: the Hardware side and the Software side.

If you are interested in the implementation of the robot, please consult `Code Base`_ to get more information.

.. _Code Base: https://github.com/haoweiqiu/Thomas-The-EV3-Engine


Hardware
-----------------

Possible Design

- Spring launcher: Uses a spring to store energy from the rotation of the motors, and releases when the programed tension is reached. Allows for simple conversion of energy between the motor and the spring, and should be repeatable over multiple attempts. 
- Catapult launcher: Uses an arm powered by 2 motors to fire the ball a distance. The catapult has consistent firing distance for stationary launches; however, when movement is factored in, the results become less reliable due to the lack of instantaneous power available from the battery.
- Wheel launcher: Accelerates the wheels to a high velocity with the help of gears, then fires the ball a nominal distance. While this could be highly dependent on the availability of a motor used to release the balls to the launcher at the correct intervals. 

Reusability

- The chassis of the robot will also have to be re-designed in order to allow for a wider wheel base to have better support for the launcher. The current base is too narrow and causes the robot to not travel linearly: the motion of the robot is not exactly straight. The final robot will also need to be slightly lighter in order for its odometer to work better.

Software
-----------------

Limitation

- The code is limited in such a way that we can only run 4 threads at a time before the robot crashes, so it must be kept compact and concise. This means that the software will have to have a large portion of its function in the main thread. In the main thread, threads unnecessary at the time can be slept to free processor space to speed up operations and ensure the robot does not crash.

Reusability

- The odometer and US localization from past labs will be reused. As well, a similar navigation tool will be used from Lab 5, as well as bang bang controller from Lab 1. The launcher class will have to be rewritten due to using stored power rather than instantaneous power. 


Methodology 
-----------------

- Each design, whether software or hardware, was implemented in the current design due to its effectiveness, based on the availability of resources and reliability of each component. Tests were performed to prove the repeatability of each component over time.