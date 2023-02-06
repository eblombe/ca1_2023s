# Turtlesim CLI

## >>> echo $ROS_DISTRO
humble

## >>>ros2 run turtlesim turtlesim_node
[INFO] [1675691931.445419443] [turtlesim]: Starting turtlesim with node name /turtlesim
[INFO] [1675691931.503102464] [turtlesim]: Spawning turtle [turtle1] at x=[5.544445], y=[5.544445], theta=[0.000000]

## >>>ros2 node list
/turtlesim

## >>>ros2 topic list
/parameter_events
/rosout
/turtle1/cmd_vel
/turtle1/color_sensor
/turtle1/pose

## >>>ros2 topic echo /turtle1/pose
x: 5.544444561004639
y: 5.544444561004639
theta: 0.0
linear_velocity: 0.0
angular_velocity: 0.0
---
*repeats

## >>>rqt_graph
*brings up rqt_graph of node tree

## >>>ros2 topic list -t
/parameter_events [rcl_interfaces/msg/ParameterEvent]
/rosout [rcl_interfaces/msg/Log]
/turtle1/cmd_vel [geometry_msgs/msg/Twist]
/turtle1/color_sensor [turtlesim/msg/Color]
/turtle1/pose [turtlesim/msg/Pose]

## >>>ros2 topic list -v
Published topics:
 * /parameter_events [rcl_interfaces/msg/ParameterEvent] 2 publishers
 * /rosout [rcl_interfaces/msg/Log] 2 publishers
 * /turtle1/color_sensor [turtlesim/msg/Color] 1 publisher
 * /turtle1/pose [turtlesim/msg/Pose] 1 publisher

Subscribed topics:
 * /parameter_events [rcl_interfaces/msg/ParameterEvent] 2 subscribers
 * /turtle1/cmd_vel [geometry_msgs/msg/Twist] 1 subscriber
 
## >>>ros2 topic hz /turtle1/pose
average rate: 62.484
	min: 0.015s max: 0.017s std dev: 0.00050s window: 190
average rate: 62.501
	min: 0.015s max: 0.017s std dev: 0.00050s window: 253
*repeats
