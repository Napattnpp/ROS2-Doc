Check ROS2 version: `printenv | grep -i ROS`

Project Setup
-------------
create work space: `mkdir -p <work_spcae_name>/src` \
create package: `ros2 pkg create --build-type ament_cmake --license Apache-2.0 <package_name>` \
build package: `colcon build`, `colcon build --packages-select <package_name>` \
source the setup file: `source install/setup.bash`

ROS2
----
start node: `ros2 run <package_name> <node_name>` \
check the executables: `ros2 pkg executables <package_name>` \
show list of topic: `ros2 topic list`
