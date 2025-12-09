Check ROS2 version: `printenv | grep -i ROS`



Project Setup
-------------
Create work space: `mkdir -p <work_spcae_name>/src` \
Create package: `ros2 pkg create --build-type ament_cmake --license Apache-2.0 <package_name>` \
Build package: `colcon build`, `colcon build --symlink-install`, `colcon build --packages-select <package_name>` \
Source the setup file: `source install/setup.bash`



ROS2 Commands
----
Start node: `ros2 run <package_name> <node_name>` \
Check the executables: `ros2 pkg executables <package_name>` \
Show list of topic: `ros2 topic list`

-----
RCL: ROS Client Library \
`ros2 start `: Starts one specific node. \
`ros2 lunch `: Starts many nodes at once.



Network
-------
Install Zerotier: `curl -s https://install.zerotier.com | sudo bash` \
Join network: `sudo zerotier-cli join <YOUR_NETWORK_ID>` \
Check connection type: `sudo zerotier-cli peers`



Additional Installation
-----------------------
Install trasnsport drivers: `git clone https://github.com/ros-drivers/transport_drivers.git -b foxy` \
`sudo apt update` \
`sudo apt install ros-foxy-sdl2-vendor ros-foxy-ackermann-msgs ros-foxy-teleop-twist-joy ros-foxy-serial-driver` 

(Run once)
Install ackermann: `sudo apt install ros-foxy-ackermann-msgs` \
Install serial driver: `sudo apt install ros-foxy-serial-driver` \
Install joy: `sudo apt install ros-foxy-joy` 




Docker
------
`docker run -it --name my-ros-container ros:humble-perception` \
`source /opt/ros/humble/setup.bash` \
`docker start -ai my-ros-container`  
