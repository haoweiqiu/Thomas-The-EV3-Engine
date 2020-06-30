Requirements
============

This document explains the Scope, purpose, Constraints, user function and the performance for the robot.

If you are interested in the implementation of the robot, please consult `Code Base`_ to get more information.

.. _Code Base: https://github.com/haoweiqiu/Thomas-The-EV3-Engine


Scope
-----------------

As required by the budget, the team will have a time budget, a breakdown of which can be found in the capabilities document. The robot will have four (4) opportunities to attempt its navigation of the playing field. Each attempt will consist of the navigation, localization, and firing of the ping pong ball as previously stated.

After determining its initial position, the robot SHALL begin localization, and issue a sequence of three (3) beeps when it has finished its initial localization. 

The robot SHALL be able navigate the obstacle course regardless of its initial starting position and orientation from either Corner 1 (the Green Zone) or Corner 3 (the Red Zone).

In accordance with the project description, the robot SHALL be able to navigate its way through the tunnel so as to avoid the water portion of the playing field, which is deemed out of bounds.

Upon navigating out of the tunnel to the firing platform, the robot SHALL proceed to the firing location, stop and issue a sequence of three (3) beeps.

The robot SHALL be able to fire a ping pong ball into the bin at a varying distance, up to four (4) tiles away.

After firing all the ping pong balls, the robot SHALL return to the starting tile and issue a series of five (5) beeps. 

After receiving the instructions, the robot must be able to recognize the boundaries of the course in order to avoid entering the water regions. Failure to comply with the boundary limitations will result in a deduction of points

The robot SHALL be able to process the game parameters from the server to acquire the information needed to determine its initial location and the set-up of the playing field.


Purpose
-----------------

The purpose of this document stands to outline the requirements of the LEGO EV3 robot (hereinafter referred to as “the robot”) and cover the requirements and limitations of its navigation.

This document will serve as the reference point from the other documents associated in this set of documentation.

The playing area has dimensions of 9x15 square tiles, each measuring 30.48cm in length. Robots are not permitted into the opposing teams corners, and must begin by localizing in their corner. During the gameplay, the robot must cross from its initial corner to the firing platform by going through a tunnel, reaching the firing location, launching a ping pong ball into a bin, and return to its starting corner. 


Constraints
-----------------

All computations are to be completed on the EV3 brick(s): no offloading to an external machine is permitted. The EV3 brick can store a total of 8V and therefore must be able to complete the obstacle course within that constraint. 

A total of 5 minutes is given for the robot to complete its objective. This means that the robot must be able to function in an appropriate manner for the entirety of its operation.

The EV3 Brick contains 4 motor ports and 4 sensor ports. While it is possible to use less motors or sensors, the maximum amount of motors and sensors is preset. The ports may be used by any of the parts that were given in the LEGO kits. This means that the client has restricted the robot’s hardware to be constructed from a selection of 6 NXT motors, 6 EV3 Motors, 3 small motors, 3 light sensors, 3 ultrasonic sensors, and 3 touch sensors. Extra components may be permitted; however, they must come with written discretion from the client.


User Function
-----------------

Before the time of demo, the user is to connect to the Wi-Fi in order to receive the game parameters of which the robot will use to help configure its navigation and define the boundaries of the playing field. After the robot has been placed on the playing field, the user will no longer be able to interact with the robot


Performance
-----------------

- The robot must be able to navigate to a point where it can successfully fire the ping pong ball into the bin. After the run, the robot must return to the starting corner, halt, and issue a sequence of 5 beeps. 
- The target can be located at a distance between 1 and 4 tiles from the in bounds playing field. Therefore, the robot will need to adjust its firing location and parameters to ensure that it can reach the target.