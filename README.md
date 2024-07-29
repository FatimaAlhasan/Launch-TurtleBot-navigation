# Launch-TurtleBot-navigation
Launch TurtleBot navigation is the software processes that enable a TurtleBot robot to navigate autonomously.

# 1- install TurtleBot package 

     sudo apt update
	   sudo apt install ros-noetic-turtlebot3 ros-noetic-turtlebot3-simulations
![‏‏لقطة الشاشة (66)](https://github.com/user-attachments/assets/63517891-892a-4c32-9726-ed249fa1ed12)

# 2- install TurtleBot simulation package


    sudo apt install ros-noetic-turtlebot3-simulations
![‏‏لقطة الشاشة (65)](https://github.com/user-attachments/assets/4ccdb127-c5da-4547-a65e-10d9bf4bea5d)

# 3- Create map and launch navigation
-Launch the TurtleBot3 world:
    
    roslaunch turtlebot3_gazebo turtlebot3_world.launch
    
![‏‏لقطة الشاشة (64)](https://github.com/user-attachments/assets/2ad781a1-30ec-4790-bb0c-60b26f05d2f4)
  
  -Launch the SLAM node:
  

    roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
   
    
![‏‏لقطة الشاشة (68)](https://github.com/user-attachments/assets/84ce9ff4-9d97-492b-b5da-4e78e78a75e4)
# save the created map

    rosrun map_server map_saver -f ~/map

-launch the teleoperation node:

    roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

# 4-Launch Navigation
-Run Navigation node

    roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
      
![‏‏لقطة الشاشة (74)](https://github.com/user-attachments/assets/7ff156fb-2090-4b7e-99c7-ec4364c3feaa)


    

