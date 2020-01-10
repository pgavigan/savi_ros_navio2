# savi_ros_navio2
Connection scripts for SAVI and the Navio2 components to work together.

Based on these tutorials:
https://github.com/emlid/mavros-navio-python-example
https://docs.emlid.com/navio2/common/dev/ros/

Setup prodeedure: Git pull this into a catkin workspace and call catkin_make. You should be good to go from there.

1) Run ardupilot and mavros as per instructions in links above.
2) rosrun savi_ros_navio2 navioPerceptions.py
