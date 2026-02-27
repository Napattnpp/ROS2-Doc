# F110th

# First Setup
```
sudo apt update && rosdep update
sudo apt install ros-$ROS_DISTRO-diagnostic-updater
rosdep install --from-paths src --ignore-src -y
colcon build
```

## Foxglove bridge / ROS bridge
- `sudo apt install ros-$ROS_DISTRO-foxglove-bridge`
> [!NOTE]
> Distributions older than Humble: `sudo apt install ros-foxy-rosbridge-server`


## Micro ROS
- **Download micro-ROS agent packages:** `ros2 run micro_ros_setup create_agent_ws.sh`
- **Build step:**
    ```
    ros2 run micro_ros_setup build_agent.sh
    source install/local_setup.bash
    ```


# Execute
- ## Run F1 tenth stack
    - `ros2 launch f1tenth_stack bringup_launch.py`

- ## Run micro ros
    - `ros2 run micro_ros_agent micro_ros_agent serial --dev /dev/ttyACM0`

- ## Run Foxglove bridge / ROS bridge
    - ***Foxglove bridge:*** `ros2 launch foxglove_bridge foxglove_bridge_launch.xml`
    - ***ROS bridge:*** `ros2 launch rosbridge_server rosbridge_websocket_launch.xml`


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
