Working Video in youtube : https://youtu.be/5cZeofgYe_g

Repo:

I have uploaded my packages in the repository.

Step1: Gitclone this repository in your SRC inside your workspace.

Step2: Now you'll have yourworkspace -> src -> tb3_sim and tb3_autonomy

Step3: Colcon package, source it. 

Step4: Run the tb3_sim launch tb3 world, run the nav2 commands for navigation starters, run the tb3_autonomy.cpp to execute.

In sequence:

colcon build

source install/setup.bash

ros2 launch tb3_sim turtlebot3_world.launch.py 

[ Create your own map or use existing map.yaml and paste the location in below command :: resource to create map : https://www.youtube.com/watch?v=QP-cxh8qUJQ&pp=ygURbWFwIGNyZWF0aW9uIHJvczI%3D ]

ros2 launch nav2_bringup bringup_launch.py use_sim_time:=True autostart:=True map:=/home/dhanush/map.yaml

ros2 run rviz2 rviz2 -d $(ros2 pkg prefix nav2_bringup)/share/nav2_bringup/rviz/nav2_default_view.rviz

ros2 launch tb3_autonomy autonomy.launch.py 

