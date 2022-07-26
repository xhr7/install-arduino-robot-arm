
install source code:

git clone https://github.com/kira-Developer/arduino_robot_arm.git

Dependencies:
run this instruction inside your workspace:

ake sure you installed all these packages:

for kinetic distro

1- $ sudo apt-get install ros-kinetic-moveit

2- $ sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui

3- $ sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher

4- $ sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control

 for melodic distro

1- $ sudo apt-get install ros-melodic-moveit

2- $ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui

3- $ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher

4- $ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control

for noetic distro

1- $ sudo apt-get install ros-noetic-moveit

2- $ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui

3- $ sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher

4- $ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control

Configuring Arduino with ROS
- Install Arduino IDE in Ubuntu https://www.arduino.cc/en/software to install run $ sudo ./install.sh after unzipping the folder

- Launch the Arduino IDE

- Install the arduino package and ros library http://wiki.ros.org/rosserial_arduino/Tutorials/Arduino%20IDE%20Setup

Usage

Controlling the robot arm by joint_state_publisher

- $ roslaunch robot_arm_pkg check_motors.launch

You can also connect with hardware by running:

- $ rosrun rosserial_python serial_node.py _port:=/dev/ttyUSB0 _baud:=115200

(Note: You may need to use ttyACM)

Simulation
Run the following instructions to use gazebo

1- $ roslaunch robot_arm_pkg check_motors.launch

2- $ roslaunch robot_arm_pkg check_motors_gazebo.launch

3- $ rosrun robot_arm_pkg joint_states_to_gazebo.py

(You may need to change the permission)

- $ sudo chmod +x ~/catkin_ws/src/arduino_robot_arm/robot_arm_pkg/scripts/joint_states_to_gazebo.py

Controlling the robot arm by Moveit and kinematics

- $ roslaunch moveit_pkg demo.launch

You can also connect with hardware by running:

- $ rosrun rosserial_python serial_node.py _port:=/dev/ttyUSB0 _baud:=115200

(Note: You may need to use ttyACM)

Simulation
Run the following instruction to use gazebo:

- $ roslaunch moveit_pkg demo_gazebo.launch


![WhatsApp Image 2022-07-26 at 7 26 12 AM](https://user-images.githubusercontent.com/102740867/180922951-ad0eb77a-6d55-43b3-a504-61d6bfff0496.jpeg)
![WhatsApp Image 2022-07-26 at 7 26 08 AM](https://user-images.githubusercontent.com/102740867/180922967-4cd01312-3991-4b76-992e-3759c67f800c.jpeg)



