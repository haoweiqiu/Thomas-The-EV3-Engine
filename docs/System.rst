System
============

The System report is composed of 5 parts: the Hardware side, the Software side, the reusability, the structure and the methodology.

If you are interested in the implementation of the robot, please consult `Code Base`_ to get more information.

.. _Code Base: https://github.com/haoweiqiu/Thomas-The-EV3-Engine


HARDWARE AVAILABILITIES AND CAPABILITIES
-----------------

- The physical hardware that we will be using for this project is LEGO. The LEGO, while good for attaching things in a linear fashion, does not do well with curved pieces which may be an issue with hardware design. 

- One of the biggest issues in the design of the robot is deciding how to create a launch system. As discussed in the Hardware Design document, 3 possibilities for a launcher have been proposed:

- Spring launcher: Uses a spring to store energy from the rotation of the motors, and releases when the programed tension is reached. Allows for simple conversion of energy between the motor and the spring, and should be repeatable over multiple attempts. 
- Catapult launcher: Uses an arm powered by 2 motors to fire the ball a distance. The catapult has consistent firing distance for stationary launches; however, when movement is factored in, the results become less reliable due to the lack of instantaneous power available from the battery.
- Wheel launcher: Accelerates the wheels to a high velocity with the help of gears, then fires the ball a nominal distance. While this could be highly dependent on the availability of a motor used to release the balls to the launcher at the correct intervals. 

SOFTWARE AVAILABLE AND CAPABILITIES
-----------------

- The code is limited in such a way that we can only run 4 threads at a time before the robot crashes, so it must be kept compact and concise. This means that the software will have to have a large portion of its function in the main thread. In the main thread, threads unnecessary at the time can be slept to free processor space to speed up operations and ensure the robot does not crash.

- The processor that is available to us is the TI Sitara AM1808 300Mhz processor from the EV3 brick. As this is a relatively outdated processor, it will cause limitations in the software design of this project.

REUSABILITY
-----------------

Software
- The odometer and US localization from past labs will be reused. As well, a similar navigation tool will be used from Lab 5, as well as bang bang controller from Lab 1. The launcher class will have to be rewritten due to using stored power rather than instantaneous power. 

Hardware
- The chassis of the robot will also have to be re-designed in order to allow for a wider wheel base to have better support for the launcher. The current base is too narrow and causes the robot to not travel linearly: the motion of the robot is not exactly straight. The final robot will also need to be slightly lighter in order for its odometer to work better; the Lab 5 robot odometer was unable to navigate correctly due to the addition in weight of the launcher when compared from Lab 3. 

STRUCTURES 
-----------------
- The maximum dimensions of the robot in order to fit through the tunnel are listed in requirements 24 and 26, with requirement 34 being made easier to achieve if the design of the robot becomes more compact.

METHODOLOGIES 
-----------------

- The software for the design consists of having 4 different threads running concurrently: navigation, the odometer, the localizer, and the odometry correction. A more detailed description of each thread and how they work together can be found in the software design document. 
- For the hardware design, 3 proposals were put forward with regards with how to build the launcher: a spring based launcher, an elastic band based launcher, and an instantaneous motor driven launcher. More details with pros and cons of each can be found in the hardware design document. 
- Each design, whether software or hardware, was implemented in the current design due to its effectiveness, based on the availability of resources and reliability of each component. Tests were performed to prove the repeatability of each component over time.

.. csv-table:: methodology list
   :header: "List of Problems", "Possible Solutions", "Final Decision"
   :widths: 20, 20, 20

   "1. Threads to be implemented", "Maximum 4 threads", "Odometer, Lightsensor, USPoller, Game – most functions run in game, sensors are used for obstacle avoidance and localization."
   "2. Launcher ", "Spring/Catapult/Wheel", "Spring: it is the easiest to implement, allows for extra motor for US sensor."
   "3. Avoidance for obstacles versus opponent’s robot", "Bang Bang controller/P-Type controller", "Bang Bang: best for consistent avoidance of obstacles"