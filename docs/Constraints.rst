Constraints
============

This document explains the constrains found for the design project. There are 3 major parts: Environmental, Hardware and Software.

If you are interested in the implementation of the robot, please consult `Code Base`_ to get more information.

.. _Code Base: https://github.com/haoweiqiu/Thomas-The-EV3-Engine


Environmental
-----------------

- The robot shall be able to operate independently of the ambient setting. The main difference between the test room and the demo room is the change in lighting intensities. This will be an issue for the light sensor: the band for measuring change in intensities must be made such that the light sensor can detect black lines in any lighting environment. 


Hardware
-----------------

- Each team is given access to the totality of the LEGO parts and components used from each of the 3 groups from the previous laboratory pairings. Additional parts may be machined for the robot if deemed necessary with written permission from the client. 


Software
-----------------

- The program will be written in Java using the leJOS program, and should be referred to for more details about its dependencies. Java compiles code to bytecode before it runs, allowing it to run both on a computer and on the EV3 brick.