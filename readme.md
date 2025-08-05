# NAVODILA

Ta postopek opisuje kako krmiliti DOBOT-a CR5 z uprabo ROS2 Humble okolja.

# 1. Vzpostavitev povezave z dobotom:
ros2 launch cr_robot_ros2 dobot_bringup_ros2.launch.py

Ta ukaz deluje le, če je robot povezan s pravilnim IP-jem

# 2. Zaženi MoveIt:
ros2 launch dobot_moveit dobot_moveit.launch.py

# 3. PowerON:
ros2 service call /dobot_bringup_ros2/srv/PowerOn dobot_msgs_v4/srv/PowerOn "{}"

# 4. Enable the robot:
ros2 service call /dobot_bringup_ros2/srv/EnableRobot dobot_msgs_v4/srv/EnableRobot "{}"

# 5. Disable the robot:
ros2 service call /dobot_bringup_ros2/srv/DisableRobot dobot_msgs_v4/srv/DisableRobot

# 6. Clear Error:
ros2 service call /dobot_bringup_ros2/srv/ClearError dobot_msgs_v4/srv/ClearError "{}"

# 7. Get error ID:
ros2 service call /dobot_bringup_ros2/srv/GetErrorID dobot_msgs_v4/srv/GetErrorID "{}"
