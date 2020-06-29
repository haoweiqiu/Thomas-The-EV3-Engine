Constraints
============

This document explains the constrains found for the design project. There are 5 major parts: Environmental issues, Hardware constraints, Software constraints, Availabilities of resources and Budget.

If you are interested in the implementation of the robot, please consult `Code Base`_ to get more information.

.. _Code Base: https://github.com/haoweiqiu/Thomas-The-EV3-Engine


Environmental issues
-----------------

- The robot shall be able to operate independently of the ambient setting. The main difference between the test room and the demo room is the change in lighting intensities. This will be an issue for the light sensor: the band for measuring change in intensities must be made such that the light sensor can detect black lines in any lighting environment. 


Hardware constraints
-----------------

- Each team is given access to the totality of the LEGO parts and components used from each of the 3 groups from the previous laboratory pairings. Additional parts may be machined for the robot if deemed necessary with written permission from the client. 


Software constraints
-----------------

- The program will be written in Java using the leJOS program, and should be referred to for more details about its dependencies. Java compiles code to bytecode before it runs, allowing it to run both on a computer and on the EV3 brick.


Availabilities of resources
-----------------

- The exact allocation of hours to each task can be found a referenced in the Gantt chart. Although subject to change, this can be used as a reference for the estimated time for each component of the project, and the resources that will be allocated to each task. 

- The critical path task could have issues in the design process for building a mechanism that is able to fire the ping pong ball. This will be the most important part of the hardware design, and the parameters of the software will have to be modified accordingly to account for the changes in weight and distribution of LEGO components. This would also lead to a large change in the documentation, creating the necessity to update relevant sections on design as well as possible modifications to the requirements.  

Budget
-----------------

- Each member will follow the tasks and responsibilities respective to their assigned tasks to the best of their abilities. In the extraordinary case that a given task may need more hours to be completed on time than the current team member assigned to that task has available, other team members who have time available may offer assistance to aid in completing the given task on time while staying within budget.