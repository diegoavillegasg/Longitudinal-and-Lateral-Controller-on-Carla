# Longitudinal-and-Lateral-Controller-on-Carla
Implementation of a Longitudinal and Lateral controller (2D) of an autonomous vehicle on Carla Simulator

In this file: https://github.com/diegoavillegasg/Longitudinal-and-Lateral-Controller-on-Carla/blob/master/controller2d.py
you will find, inside the method: *update_controls*, a PID controller implementation for the **longitudinal control** and
the **lateral control** of a vehicle that should follow a serie of a waypoints
including the velocity at each waypoint.

For the **lateral control** we have followed the Stanley method.
Explained in section 2.3 here: *https://www.ri.cmu.edu/pub_files/2009/2/Automatic_Steering_Methods_for_Autonomous_Automobile_Path_Tracking.pdf*

In other words, these two controllers are the result like a human driver performs while driving: to brake,
move forward, turn the steering wheel, ... etc.

The inputs are:
- the current position in 2d coordinates (X and Y, [m]),
- the current velocity (V [m/s]),
- the current yaw pose angle (YAW [rad]),
- the list of waypoints (X [m], Y[m], V[m/s]).

Whilst the output are, (note that are the same that a human driver would give to control a car):
- the engine throttle (a decimal value from 0 to 1),
- the steering angle (a value from -1.22 rad to 1.22 rad),
- the brake (a decimal value from 0 to 1).

![alt text](https://github.com/diegoavillegasg/Longitudinal-and-Lateral-Controller-on-Carla/blob/master/Screenshot%20from%202019-11-11%2020-02-58.png)

![alt text](https://github.com/diegoavillegasg/Longitudinal-and-Lateral-Controller-on-Carla/blob/master/Screenshot%20from%202019-11-11%2020-04-04.png)
