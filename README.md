# ROS Gazebo Simulation Model

A ROS package for gazebo simulation of a small four wheeled skid steering robot model.

Current Plugins : skid_steering, laser

# HOW TO USE

Clone the package in your catkin_workspace


#### $ cd catkin_ws/src

#### $ git clone https://github.com/Keshav-31/model

#### $ cd ..

##### $ catkin_make

Launching the gazebo Simulation

##### $ roslaunch model gazebo.launch

This launches the gazebo simulations in the empty world with the laser and skid steering plugins.
The command Topic for the skid_steering is cmd_vel
To launch the teleop use:

##### $ roslaunch model teleop.launch

Use the arrow keys to control the model.

# SLAM

Use the mapping.launch for mapping. It uses hector mapping to create a map using the laser scan data.
Befor using mapping.launch, first build a world in gazebo around the robot otherwise it won't work.
After creating a world use
 
##### $ roslaunch model gmapping.launch

Then use the display.launch file to open Rviz with the robot state publisher and add Map in Rviz with the topic /map.
Now, use teleop to move the robot in gazebo and a map would be generated in Rviz.

# Navigation

##### $ roslaunch model gazebo.launch
##### $ roslaunch model display.launch
( Then create a world in gazebo using building editor.)

##### $ roslaunch model gmapping.launch
##### $ roslanch model model_navigation.launch

Then use the 2D Nav Goal in rviz to send goals to move_base.

The configuration files for the move_base are present in the config folder. To fine tune the navigation make changes in the paramter files accordingly.
  
