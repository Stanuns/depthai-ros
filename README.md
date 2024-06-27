# Depthai ROS Repository
Hi and welcome to the main depthai-ros respository! Here you can find ROS related code for OAK cameras from Luxonis. Don't have one? You can get them [here!](https://shop.luxonis.com/)

You can find the newest documentation [here](https://docs.luxonis.com/software/ros/depthai-ros/)

# Run OAK-D S2 [here](https://docs.luxonis.com/software/ros/depthai-ros/build/)
- install dependencies and Setting up procedure

```bashrc
sudo wget -qO- https://raw.githubusercontent.com/luxonis/depthai-ros/main/install_dependencies.sh | sudo bash 
```

```bashrc
sudo apt install libopencv-dev python3-colcon-common-extensions -y
mkdir -p depthai_ws/src
cd depthai_ws/src
git clone --branch humble git@github.com:Stanuns/depthai-ros.git ## https://github.com/luxonis/depthai-ros.git
cd ..
rosdep install --from-paths src --ignore-src -r -y
colcon build
source install/setup.bash
```

- run oAK-D S2 camera
```
ros2 launch depthai_ros_driver rgbd_pcl.launch.py
```