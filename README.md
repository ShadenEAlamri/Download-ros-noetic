# Download-ros-noetic
# ROS Installation Guide

This guide provides instructions for installing ROS Noetic and ROS 2 Humble on Ubuntu.

## Prerequisites

- **OS**: Ubuntu 20.04 (Focal Fossa) for ROS Noetic; Ubuntu 22.04 (Jammy Jellyfish) for ROS 2 Humble.
- **Requirements**: Minimum 2 GB RAM and 10 GB disk space.

## Installing ROS Noetic

1. **Set Up Sources**:
   ```bash
   sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros-latest.list'
   ```

2. **Set Up Keys**:
   ```bash
   sudo apt update
   sudo apt install -y curl
   curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.key | sudo apt-key add -
   ```

3. **Install ROS Noetic**:
   ```bash
   sudo apt update
   sudo apt install -y ros-noetic-desktop-full
   ```

4. **Environment Setup**:
   ```bash
   echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
   source ~/.bashrc
   ```

5. **Install Dependencies**:
   ```bash
   sudo apt install -y python3-rosdep
   sudo rosdep init
   rosdep update
   ```

## Installing ROS 2 Humble

1. **Set Up Sources**:
   ```bash
   sudo apt update && sudo apt install -y software-properties-common
   sudo add-apt-repository universe
   ```

2. **Set Up Keys**:
   ```bash
   curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.key | sudo apt-key add -
   ```

3. **Install ROS 2 Humble**:
   ```bash
   sudo apt update
   sudo apt install -y ros-humble-desktop
   ```

4. **Environment Setup**:
   ```bash
   echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
   source ~/.bashrc
   ```

5. **Install Dependencies**:
   ```bash
   sudo apt install -y python3-rosdep
   sudo rosdep init
   rosdep update
   ```

## Verification

- For ROS Noetic:
  ```bash
  roscore
  ```
- For ROS 2 Humble:
  ```bash
  ros2 run demo_nodes_cpp talker
  ```

## Conclusion

You have successfully installed ROS Noetic and ROS 2 Humble. Refer to the official documentation for more information:

- [ROS Noetic Documentation]
- [ROS 2 Humble Documentation]

Happy coding
