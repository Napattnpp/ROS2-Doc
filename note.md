source /opt/ros/<your_distro>/setup.bash
export ROS_DOMAIN_ID=0
export RMW_IMPLEMENTATION=rmw_fastrtps_cpp
ros2 run micro_ros_agent micro_ros_agent serial --dev /dev/ttyACM0 -v6

source /opt/ros/<your_distro>/setup.bash
export ROS_DOMAIN_ID=0
export RMW_IMPLEMENTATION=rmw_fastrtps_cpp
ros2 daemon stop
ros2 daemon start
ros2 topic list -t

ros2 bag record \
/tf /tf_static \
/imu/data \
/odom \
/odometry/filtered \
/sensors/core \
/commands/servo/position \
/commands/motor/speed


------------------

b15644912e7b3cd5
https://drive.google.com/drive/folders/1N0xOtJzdbNTUE-D_Xjko-mrmlc9OgNMI?usp=share_link

> [!NOTE]
> This is a note

> [!TIP]
> This is a tip

> [!IMPORTANT]
> This is important information

> [!WARNING]
> This is a warning

> [!CAUTION]
> This is a caution

> [!NOTE]
> ***Distributions $\color{red}{\text{older than}}$ Humble:*** `sudo apt install ros-foxy-rosbridge-server`
