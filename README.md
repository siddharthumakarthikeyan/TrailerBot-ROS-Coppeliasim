# TrailerBot ROS Coppeliasim
## SLAM of Trailer based Autonomous Ground Vehicle using ROS and Coppeliasim

<object width="425" height="350">
  <param name="movie" value="http://www.youtube.com/user/wwwLoveWatercom?v=BTRN1YETpyg" />
  <param name="wmode" value="transparent" />
  <embed src="http://www.youtube.com/user/wwwLoveWatercom?v=BTRN1YETpyg"
         type="application/x-shockwave-flash"
         wmode="transparent" width="425" height="350" />
</object>

### System Dependencies
- Ubuntu : 16.04+
- ROS : Kinetic+
- CPU : ARM7+ or Intel i3+ or AMD R4+
- RAM : 4GB+
- Memory : 10GB+

### Dependencies

- ```sudo apt install ros-noetic-geographic-msgs```
- ```sudo apt install ros-noetic-turtlebot3-msgs```
- ```sudo apt install ros-noetic-control-msgs```
- ```sudo apt install ros-noetic-octomap-server```
- ```sudo apt install ros-noetic-move-base```
- ```sudo apt install ros-noetic-dwa-local-planner```
- ```sudo apt install ros-noetic-global-planner```
- ```sudo apt install ros-noetic-map-server```
- ```sudo apt install ros-noetic-explore-elite```
- ```sudo apt install xterm```


### steps to runs 
*note* Run the scripts in the following sequence

- Terminal 1 -
    - source ~/<YOUR_FOLDER_NAME>/devel/setup.bash
    - roscore
    
- Terminal 2 -
    - source ~/<YOUR_FOLDER_NAME>/devel/setup.bash
    - cd Coppeliasim/
    - ./coppeliasim.sh (launches coppelia sim)
    - load the scene from `~/<YOUR_FOLDER_NAME>/src/coppeliasim_ws/vrep_scenes/`
    
- Terminal 3 -
    - source ~/<YOUR_FOLDER_NAME>/devel/setup.bash
    - roslaunch coppeliasim_ws teleop.launch
    
- Terminal 4 -
    - source ~/<YOUR_FOLDER_NAME>/devel/setup.bash
    - roslaunch coppeliasim_ws mapping.launch
    
- Terminal 5 -
    - source ~/<YOUR_FOLDER_NAME>/devel/setup.bash
    - rviz
    - load tf, map and laser topic

