
`git clone https://github.com/hwyao/FLIQC_example_workspace_ros.git`

`cd FLIQC_example_workspace_ros`

`git checkout feature/init_controllers`

`git submodule update --init --recursive`

`git submodule update --remote --merge`

`cd src`

-----------------------------------
update the subpackages

`cd fliqc_controller_ros/`

`git checkout feature/fliqc_standard_controller`

`git pull`

-----------------------------------
`cd robot_env_publisher/`

`git checkout feature/switch_to_PlanningSceneMonitor`

`git pull`

-----------------------------------
`cd multi_agent_vector_fields/`

`git checkout feature/fliqc_control_standard`

`git pull`

-----------------------------------

install moveit 

`sudo apt install ros-noetic-moveit` 

-----------------------------------

install the franka package in src folder 

`cd ~/FLIQC_example_workspace_ros/src`  

`git clone --branch develop https://github.com/frankaemika/franka_ros.git`


-----------------------------------
install pinocchio

Following the link: `https://stack-of-tasks.github.io/pinocchio/download.htm`

-----------------------------------

install rosdep 
Following the link`http://wiki.ros.org/rosdep`

-----------------------------------

After that the workspace should be like this 

![image](https://github.com/user-attachments/assets/a84e84d7-fa3b-4947-aeeb-a50db58024b8)

-----------------------------------

`catkin build`

after catkin build , errors will appear.

Now delete the folder build by path 
`src/fliqc_controller_ros/submodule/FLIQC_controller_core/external/build`

`catkin clean` and `catkin build` again

-----------------------------------

## If we want to change the obstacle env

![image](https://github.com/user-attachments/assets/f55c2d19-fad3-4fe9-a054-091d10770797)

change the yaml file to others. Using ` generate_wall.py`  script can change the obstacles in `obstacle_T.yaml` 

![image](https://github.com/user-attachments/assets/48e08aab-f6bd-47a1-9185-4c25fcfe16fa)


## If we want to change the goal point position

go to the ` src/multi_agent_vector_fields/config`  and change the start_goal.yaml

![image](https://github.com/user-attachments/assets/4fecdcd7-9c08-4b66-ba88-ba09854f0652)


## Expected 

![image](https://github.com/user-attachments/assets/528320c7-3cca-44a7-a7c5-4fecf33f155b)


