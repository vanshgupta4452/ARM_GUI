# Robotic Arm Control Web GUI

This web application allows real-time wireless control of a 6 Degree of Freedom (DOF) Robotic Arm. It is connected via a rosbridge server to facilitate seamless communication with the robotic arm.

## Prerequisites

Before using this application, ensure you have the following prerequisites:

- **ROS (Robot Operating System)**: Install ROS on the system that controls the robotic arm. You can find installation instructions on the [ROS official website](http://www.ros.org/).

- **rosbridge_suite**: Install the `rosbridge_suite` package to enable communication between ROS and the web GUI. You can install it by following the instructions in the [rosbridge_suite GitHub repository](https://github.com/RobotWebTools/rosbridge_suite).
## Installing rosbridge_suite

To install the `rosbridge_suite`, follow these commands:

```bash
# Install rosbridge_suite using apt
sudo apt-get install ros-<distro>-rosbridge-suite

Replace <distro> with your ROS distribution (e.g., kinetic, melodic).
```

## Usage

1. Clone this repository to your catkin workspace.


2. Source your ROS workspace
    ```bash
    source /path/to/your/ros/workspace/devel/setup.bash
    ```

3. Run the following command:
   ```bash 
    roslaunch ajgar_core arm_gui.launch
    ```
-  This command initiates and manages all essential functionalities for the robotic arm, including launching the core ROS system `roscore` and establishing a rosbridge websocket connection.


5. Open the `control_arm_GUI.html` file in your web browser.

6. Use the provided sliders to control the positions of the six joints of the robotic arm.
 
## Roslibjs
roslibjs is the standard ROS JavaScript library designed for interacting with ROS (Robot Operating System) from a web browser. 
It utilizes WebSockets to establish a connection with rosbridge, providing a communication channel for ROS functionality between the browser and the ROS environment. 
This library facilitates tasks such as subscribing to ROS topics, publishing messages, making service calls, and interacting with the ROS Parameter Server directly from a web page
You can learn more about it from [roslibjs- ROS Wiki](http://wiki.ros.org/roslibjs)

## Disclaimer

This web GUI is developed by A.T.O.M Robotic Labs for educational and testing purposes. Ensure proper safety measures are in place when operating the robotic arm. The developers are not responsible for any misuse or accidents caused by the use of this application.
