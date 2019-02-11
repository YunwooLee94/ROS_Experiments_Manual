# ROS_Experiments_Manual
practice_1

This manual has been made for robot experiments using ROS.

#Initial Setting
1. First of all, you need to set up each computer's ROS IP address.

2. Make the launch file for initialization of robots, and insert codes which declare the namespace.
(e.g. "<group ns="Robot1">, </group>")

3. Enter to packages you want to use and edit its launch file to designate topics' namespace(especially 'remap part').

#Experiments
1. (@ my_computer) Execute the 'roscore' for using master of ROS.

2. (@ my_computer) Access the robot computer using "ssh robot@robot_ip_address" (@my_computer --> @robot).

3. (@ robot) rosrun/roslaunch the all the nodes you want to use.

[From now, especially for Pioneer Control] 
4. (@ my_computer) rostopic pub /namespace/cmd_motor_ .. 'tab' 'tab' change state from 0 to 1.

5. (@ my_computer) roslaunch turtlebot_teleop keyboard_teleop.launch

[Recording]
6. rosbag record --lz4 -O test.bag /namespace/data

#After Experiments
1. You can verify your saved data using command "rosbag info <filename>" or "rosbag play <filename>".
<<<<>>>>>
