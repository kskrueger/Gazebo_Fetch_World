# Gazebo_Fetch_World
## Extra packages
```
apt install ros-noetic-robot-controllers
apt install ros-noetic-rgbd-launch
apt install ros-noetic-fetch-description
```

## Launch the world
```
catkin build
source devel/setup.bash
./start_world.sh
```

## Send drive commands to the robot
```
rostopic pub /base_controller/command geometry_msgs/Twist "linear:
  x: 0.0
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.0"
```

## View camera feed topic at:
```
rostopic echo /head_camera/rgb/image_raw
```
