
# BOOTCAMP_ROS
SLAM & SIMULTANIOUS NAVIGATION

```bash
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
```
```bash
ros2 launch turtlebot3_cartographer cartographer.launch.py use_sim_time:=true
```
```bash
ros2 run turtlebot3_teleop teleop_keyboard
```
```bash
 ros2 launch turtlebot3_navigation2 navigation2.launch.py
```

NAVIGATION WITH MAP

```bash
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
```
```bash
ros2 launch nav2_bringup localization_launch.py map:=./src/map_1727902180.yaml use_sim_time:=true
```
```bash
ros2 run rviz2 rviz2 -d /opt/ros/humble/share/nav2_bringup/rviz/nav2_default_view.rviz
```
do the estimate in rviz
change the map topic to transient_local


```bash
ros2 launch nav2_bringup navigation_launch.py use_sim_time:=true map_subscribe_transient_local:=true
```
do pose estimation if needed again
