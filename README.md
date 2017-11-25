# catkin_tester
*A pre-build local source install of the ROS navigtion stack, Turtlebot backend repositories, and dependencies*

### **Introduction**

The build configuration has been customized to compile all packages a position-independent executables/libs.
So (if it has been set up correctly), you might not nessisarily have to recompile it -- the libs and binaries,
should (in theory, anyway) be functional on your own system.


### **Build**
```
source source /opt/ros/rosdesktop_ws/devel_isolated/setup.bash
cd
git clone [this-repo]


# build external dependencies
cd ~/catkin_tester/ros_external_depends/SDL2/build
cmake ..
make

cd ~/catkin_tester/ros_external_depends/SDL_image/build
cmake ..
make

cd ~/catkin_tester/ros_external_depends/flann/build
cmake ..
make
# Now copy the files from ~/catkin_tester/ros_external_depends/flann/build/lib to ~/catkin_tester/ros_external_depends/flann/build/CMakeFiles/Export/lib

cd ~/catkin_tester/ros_external_depends/qhull/build
cmake ..
make


cd ~/catkin_tester/ros_external_depends/orocos-bayesian-filtering/build
cmake ..
make

cd ~/catkin_tester/ros_external_depends/orocos-bayesian-filtering/bfl_typekit/build
cmake ..
make

cd ~/catkin_tester/ros_external_depends/orocos-bayesian-filtering/orocos_bfl/build
cmake ..
make

cd ~/catkin_tester/ros_external_depends
git clone https://github.com/PointCloudLibrary/pcl.git
cd pcl
git checkout pcl-1.7.2
mkdir build && cd build
cmake ..
make

cd ~/catkin_tester
source devel/setup.bash
catkin_make
```

You should be good to go.  **However**, I *strongly* suggest that you link this workspace
to your catkin_ws, so that catkin_make does not re-evaluate all these packages every time
you want to rebuild your own projects
