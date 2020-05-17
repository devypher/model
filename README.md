#ROS Gazebo Simulation Model

A ROS package for gazebo simulation of a small four wheeled skid steering robot model.

Current Plugins : skid_steering, laser

#HOW TO USE

Clone the package in your catkin_workspace/src

go to the workspace and use

$ catkin_make

Launching the gazebo Simulation

$ roslaunch model gazebo.launch

This launches the gazebo simulations in the empty world with the laser and skid steering plugins.
The command Topic for the skid_steering is /turtle1/cmd_vel
So you can use the turtlesim_teleop for controlling Robot in gazebo.

$ rosrun turtlesim turtle_teleop_key

Use the arrow keys to control the model.

(if the robot topples in gazebo then tune the parameters in the skid_steering plugin in the URDF file.)
  
