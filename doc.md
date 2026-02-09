# Main
`ros2 run joy joy_node` \
`ros2 launch vesc_driver vesc_driver_node.launch.py` \
`ros2 launch vesc_ackermann vesc_to_odom_node.launch.xml` \
`ros2 launch sllidar_ros2 sllidar_s1_launch.py`


# Micro ROS
`ros2 run micro_ros_agent micro_ros_agent serial --dev /dev/ttyACM0`

# Port
`sudo chmod 777 /dev/ttyACM0` \
`echo 'KERNEL=="ttyACM*", MODE="0666"' | sudo tee /etc/udev/rules.d/99-usb-serial.rules` \
`sudo udevadm control --reload-rules && sudo udevadm trigger`
