# ROS Gazebo Simulation Model

A ROS package for gazebo simulation of a small four wheeled skid steering robot model.

Current Plugins : skid_steering, laser

# HOW TO USE

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

# SLAM

Use the mapping.launch for mapping. It uses hector mapping to create a map using the laser scan data.
Befor using mapping.launch, first build a world in gazebo around the robot otherwise it won't work.
After creating a world use
 
$ roslaunch model mapping.launch

Then use the display.launch file to open Rviz with the robot state publisher and add Map in Rviz with the topic /map.
Now, use teleop to move the robot in gazebo and a map would be generated in Rviz.
  
