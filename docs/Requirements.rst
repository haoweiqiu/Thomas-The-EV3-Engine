Requirements
============

This document explains the purpose, user function and the performance for the robot.

If you are interested in the implementation of the robot, please consult `Code Base`_ to get more information.

.. _Code Base: https://github.com/haoweiqiu/Thomas-The-EV3-Engine


Purpose
-----------------

- The purpose of this document stands to outline the requirements of the LEGO EV3 robot (hereinafter referred to as “the robot”) and cover the requirements and limitations of its navigation.
- This document will serve as the reference point from the other documents associated in this set of documentation.
- The playing area has dimensions of 9x15 square tiles, each measuring 30.48cm in length. Robots are not permitted into the opposing teams corners, and must begin by localizing in their corner. During the gameplay, the robot must cross from its initial corner to the firing platform by going through a tunnel, reaching the firing location, launching a ping pong ball into a bin, and return to its starting corner. 


User Function
-----------------

- Before the time of demo, the user is to connect to the Wi-Fi in order to receive the game parameters of which the robot will use to help configure its navigation and define the boundaries of the playing field. After the robot has been placed on the playing field, the user will no longer be able to interact with the robot


Performance
-----------------

- The robot must be able to navigate to a point where it can successfully fire the ping pong ball into the bin. After the run, the robot must return to the starting corner, halt, and issue a sequence of 5 beeps. 
- The target can be located at a distance between 1 and 4 tiles from the in bounds playing field. Therefore, the robot will need to adjust its firing location and parameters to ensure that it can reach the target.