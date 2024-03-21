# RobolabY2
Getting started
1.Clone the repo:


      git clone https://github.com/12uminations/RobolabY2.git

  
2.Navigate to your workspace:


      cd ~/huadee_ws

  
3.Downlaod Gazebo ros2 control:


      สามารถทำได้ตาม link: https://www.youtube.com/watch?v=4QKsDf1c4hc&t=1223s

  
4.Compile:


      colcon build


------------------------------------------------------------


# Operating Instructions


After you build, remember to source the proper install folder:


      cd (into your workspace)
  
      colcon build --symlink-install
  
      source install/setup.bash

  
And then run the launch file:


      ros2 launch articubot_one launch_sim.launch.py

  
After that run the this file to control robot:


      ros2 run teleop_twist_keyboard teleop_twist_keyboard

  
Run this code to control robot's mechanical arm:


      ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r /cmd_vel:=/diff_cont/cmd_vel_unstamped
