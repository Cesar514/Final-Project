# Path planning

## Commands list
Remember to always run chmod+x file.py to make the codes work
## Environment ONE Path planning with Position of human with Odometry.
This environment is supposed to allow path planning and following the human around. After this if the user starts the operation of "To paying area" the robot should be able to go to the paying area. When the battery is low, the robot

twist.py
pathPLanning.py
robotMove.py
market.yaml
market.world

> START ROSCORE
```
cd catkin_ws
roscore
```
> LOAD MAP DATA
Then open a new terminal
```
rosrun map_server map_server src/final_project/data/market.yaml
```
> LOAD MAP SCREEN
Then open a new terminal
```
rosrun stage_ros stageros src/final_project/data/market.world
```
> START TELEOP SCRIPT
Then open a new terminal
```
source devel/setup.bash
roslaunch socspioneer keyboard_teleop.launch
```
> START HUMAN MOVEMENT SCRIPT
Then open a new terminal
```
source devel/setup.bash
rosrun final_project twist.py
```
> Change parameters inside this function to account for human speed.
After this you can go to teleop window to move human. 

> SEE CONNECTED NODES
```
rosrun rqt_graph rqt_graph
```

> START RVIZ
```
rosrun rviz rviz
```
Be sure to load the corresponding .rviz file to get needed information displayed
> RUN ROBOT CONTROL
This allows the robot to be controlled by the algorithms
```
source devel/setup.bash
rosrun final_project robotMove.py
```
> RUN ASTAR
Initial path planning Algorithm
```
source devel/setup.bash
rosrun final_project pathPlanning.py
```
## Environment TWO Visual path planning (MAP 500x500)
This environment is supposed to allow path planning giving position of human based on camera robot should be following the human around. After this if the user starts the operation of "To paying area" the robot should be able to go to the paying area. When the battery is low, the robot goes to the closest battery station.

twist.py
visualPlanning.py
robotMoveVisual.py
objectMovements.py
marketMed.yaml
marketMed.world

> START ROSCORE
```
cd catkin_ws
roscore
```
> LOAD MAP DATA
```
source devel/setup.bash
rosrun map_server map_server src/final_project/data/marketMed.yaml
```
> LOAD MAP SCREEN
```
source devel/setup.bash
rosrun stage_ros stageros src/final_project/data/marketMed.world
```
> START TELEOP SCRIPT
```
source devel/setup.bash
roslaunch socspioneer keyboard_teleop.launch
```
> START HUMAN MOVEMENT SCRIPT
```
source devel/setup.bash
rosrun final_project twist.py
```
> Change parameters inside this function to account for human speed.
After this go to teleop window to move human. 
> SEE CONNECTED NODES
```
rosrun rqt_graph rqt_graph
```
> START RVIZ
```
rosrun rviz rviz
```
Be sure to load the corresponding visualproject.rviz file to get needed information displayed
> RUN ROBOT CONTROL
This allows the robot to be controlled by the algorithms
```
source devel/setup.bash
rosrun final_project robotMoveVisual.py
```
> RUN Computer Vision Tracking
```
source devel/setup.bash
rosrun final_project objectMovements.py
```

> RUN ASTAR FOR VISUAL PLANNING
Initial path planning Algorithm
```
source devel/setup.bash
rosrun final_project visualPlanning.py
```


## Environment THREE Visual path planning with prediction (MAP 500x500)
This environment is supposed to allow path planning giving position of human based on camera robot should be following the human around. After this if the user starts the operation of "To paying area" the robot should be able to go to the paying area. When the battery is low, the robot goes to the closest battery station.

twist.py
visualPlanning.py
robotMoveVisual.py
objectMovementsPredict.py
marketMed.yaml
marketMed.world

> START ROSCORE
```
cd catkin_ws
roscore
```
> LOAD MAP DATA
```
source devel/setup.bash
rosrun map_server map_server src/final_project/data/marketMed.yaml
```
> LOAD MAP SCREEN
```
source devel/setup.bash
rosrun stage_ros stageros src/final_project/data/marketMed.world
```
> START TELEOP SCRIPT
```
source devel/setup.bash
roslaunch socspioneer keyboard_teleop.launch
```
> START HUMAN MOVEMENT SCRIPT
```
source devel/setup.bash
rosrun final_project twist.py
```
> Change parameters inside this function to account for human speed.
After this go to teleop window to move human. 
> SEE CONNECTED NODES
```
rosrun rqt_graph rqt_graph
```
> START RVIZ
```
rosrun rviz rviz
```
Be sure to load the corresponding visualproject.rviz file to get needed information displayed
> RUN ROBOT CONTROL
This allows the robot to be controlled by the algorithms
```
source devel/setup.bash
rosrun final_project robotMoveVisual.py
```
> RUN Computer Vision Tracking with Prediction
```
source devel/setup.bash
rosrun final_project objectMovementsPredict.py
```

> RUN ASTAR FOR VISUAL PLANNING
Initial path planning Algorithm
```
source devel/setup.bash
rosrun final_project visualPlanning.py
```

## Environment FOUR Visual path planning with Obstacles Update (MAP 500x500)
This environment is supposed to allow path planning giving position of human based on camera robot should be following the human around. After this if the user starts the operation of "To paying area" the robot should be able to go to the paying area. When the battery is low, the robot goes to the closest battery station.

twist.py
visualPlanning.py
robotMoveVisual.py
objectMovementsRebuild.py
marketMed.yaml
marketMed.world

> START ROSCORE
```
cd catkin_ws
roscore
```
> LOAD MAP DATA
```
source devel/setup.bash
rosrun map_server map_server src/final_project/data/marketMed.yaml
```
> LOAD MAP SCREEN
```
source devel/setup.bash
rosrun stage_ros stageros src/final_project/data/marketMed.world
```
> START TELEOP SCRIPT
```
source devel/setup.bash
roslaunch socspioneer keyboard_teleop.launch
```
> START HUMAN MOVEMENT SCRIPT
```
source devel/setup.bash
rosrun final_project twist.py
```
> Change parameters inside this function to account for human speed.
After this go to teleop window to move human. 
> SEE CONNECTED NODES
```
rosrun rqt_graph rqt_graph
```
> START RVIZ
```
rosrun rviz rviz
```
Be sure to load the corresponding visualproject.rviz file to get needed information displayed
> RUN ROBOT CONTROL
This allows the robot to be controlled by the algorithms
```
source devel/setup.bash
rosrun final_project robotMoveVisual.py
```
> RUN Computer Vision with MAP REBUILD
```
source devel/setup.bash
rosrun final_project objectMovementsRebuild.py
```

> RUN ASTAR FOR VISUAL PLANNING
Initial path planning Algorithm
```
source devel/setup.bash
rosrun final_project visualPlanning.py
```

## Environment FIVE Visual path planning with Obstacles Update and prediction(MAP 500x500)
This environment is supposed to allow path planning giving position of human based on camera robot should be following the human around. After this if the user starts the operation of "To paying area" the robot should be able to go to the paying area. When the battery is low, the robot goes to the closest battery station.

twist.py
visualPlanning.py
robotMoveVisual.py
objectMovementsFull.py
marketMed.yaml
marketMed.world

> START ROSCORE
```
cd catkin_ws
roscore
```
> LOAD MAP DATA
```
source devel/setup.bash
rosrun map_server map_server src/final_project/data/marketMed.yaml
```
> LOAD MAP SCREEN
```
source devel/setup.bash
rosrun stage_ros stageros src/final_project/data/marketMed.world
```
> START TELEOP SCRIPT
```
source devel/setup.bash
roslaunch socspioneer keyboard_teleop.launch
```
> START HUMAN MOVEMENT SCRIPT
```
source devel/setup.bash
rosrun final_project twist.py
```
> Change parameters inside this function to account for human speed.
After this go to teleop window to move human. 
> SEE CONNECTED NODES
```
rosrun rqt_graph rqt_graph
```
> START RVIZ
```
rosrun rviz rviz
```
Be sure to load the corresponding visualproject.rviz file to get needed information displayed
> RUN ROBOT CONTROL
This allows the robot to be controlled by the algorithms
```
source devel/setup.bash
rosrun final_project robotMoveVisual.py
```
> RUN Computer Vision with MAP REBUILD and Prediction
```
source devel/setup.bash
rosrun final_project objectMovementsFull.py
```

> RUN ASTAR FOR VISUAL PLANNING
Initial path planning Algorithm
```
source devel/setup.bash
rosrun final_project visualPlanning.py


### EXTRA Test Worlds (LARGE) for testing positions
```
rosrun stage_ros stageros src/final_project/data/Worlds/LARGEMAP/market#.world
```
> Remember to check speeds comparison for Manhattan and Euclidean Distance and optimal heuristics
