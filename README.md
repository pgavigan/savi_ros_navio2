# savi_ros_navio2
Connection scripts for SAVI and the Navio2 components to work together.

Based on these tutorials:
https://github.com/emlid/mavros-navio-python-example
https://docs.emlid.com/navio2/common/dev/ros/

Setup prodeedure: Git pull this into a catkin workspace and call catkin_make. You should be good to go from there.

1) Run ardupilot and mavros as per instructions in links above. Extracted from those links is the following:

Start ROS
```Run roscore```

Start arducoper
```
sudo systemctl start arducopter
sudo systemctl enable arducopter
```

Start MavROS
```
pi@navio: ~ $ rosrun mavros mavros_node \
_fcu_url:=udp://:14650@ \
_gcs_url:=udp://:14551@192.168.1.189:14550
```

Setup MavROS to work without a ground station. This sets a steam rate (I don't know what that means).
```rosservice call /mavros/set_stream_rate 0 10 1```

2) Run the new node
```rosrun savi_ros_navio2 navioPerceptions.py```
