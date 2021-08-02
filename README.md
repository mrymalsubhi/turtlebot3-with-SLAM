# turtlebot3-with-SLAM
## task 2
- this work with ubuntu 18.04 OS and ROS melodic.

--- 

- 1st: step: in the terminal write this code to install turtlebot3 packages:

```sudo apt-get install ros-melodic-dynamixel-sdk
 sudo apt-get install ros-melodic-turtlebot3-msgs
 sudo apt-get install ros-melodic-turtlebot3 
 ```

---

- 2nd step: install Simulation packages:
```cd ~/catkin_ws/src/
$ git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make
```
---

- 3rd step: write this code:
``` source ~/catkin_ws/devel/setup.bash 
```

---
- 4th step: open a new terminal from file - new tap. 

---

- 5th step: after you opend a new terminal, now you are ready to launch Simulation World by typing this code: 

``` export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_gazebo turtlebot3_world.launch 
```
now the gazebo will work as it shown in the photo.

![IMG_6876](https://user-images.githubusercontent.com/85639068/127822641-2ec40fd2-fa49-4591-b917-7dda6c02b3ab.jpg)

---
- 6th step: open a new terminal from file - new tap. Control the robot movement by typing this code:
``` export TURTLEBOT3_MODEL=waffle_pi

roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
![IMG_6877](https://user-images.githubusercontent.com/85639068/127823178-5c49cc51-cb14-4c51-9c91-901887105f23.jpg)

- 7th step: Launch the SLAM Node: in a new terminal file - new tap. run this code:
``` export TURTLEBOT3_MODEL=burger
 roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping 
```
![IMG_6879](https://user-images.githubusercontent.com/85639068/127823740-010bffa2-179e-46b8-91ab-5fbb463d84ed.jpg)

---
- 8th step: and finally to save the map, run this code: 
``` rosrun map_server map_saver -f ~/map
```
![IMG_6880](https://user-images.githubusercontent.com/85639068/127824221-efa94ac5-698d-4bcb-9224-a91ec10df713.jpg)

---

- and this is how it will look like.


---

![IMG_6881](https://user-images.githubusercontent.com/85639068/127824373-353134f3-1e8b-4680-bc41-371f403c270a.jpg)
 




