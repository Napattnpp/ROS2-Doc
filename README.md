sudo apt update && sudo apt upgrade -y

----

sudo apt install -y \
  build-essential cmake git wget curl gnupg2 lsb-release \
  python3-pip python3-colcon-common-extensions python3-vcstool
  
----

sudo apt install -y \
  libasio-dev libtinyxml2-dev libcunit1-dev \
  liblog4cxx-dev libyaml-cpp-dev libeigen3-dev \
  python3-empy python3-numpy python3-yaml python3-netifaces

----

mkdir -p ~/ros2_foxy/src
cd ~/ros2_foxy

----

wget https://raw.githubusercontent.com/ros2/ros2/foxy/ros2.repos
vcs import src < ros2.repos

----

cd ~/ros2_foxy/src
git clone https://github.com/ros2/rolling-bionic-patches.git
~/ros2_foxy/src/rolling-bionic-patches/apply_patches.sh ~/ros2_foxy

----

sudo apt install -y ros-foxy-cyclonedds
echo "export RMW_IMPLEMENTATION=rmw_cyclonedds_cpp" >> ~/.bashrc

----

cd ~/ros2_foxy
colcon build --symlink-install

colcon build --executor sequential

----

echo "source ~/ros2_foxy/install/setup.bash" >> ~/.bashrc

source ~/ros2_foxy/install/setup.bash
