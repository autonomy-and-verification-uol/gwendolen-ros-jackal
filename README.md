# gwendolen-ros-jackal
Examples of a Gwendolen agent autonomously controlling a Clearpath Jackal UGV.

Requires [gwendolen-rosbridge](https://github.com/autonomy-and-verification-uol/gwendolen-rosbridge) to be installed and working.

Also requires Jackal ROS packages to be installed. Make sure to install [jackal main files](https://gist.github.com/vfdev-5/57a0171d8f5697831dc8d374839bca12) (You can test if it installed correctly with the commands in the "Start simulation" section of that link, however you do not have to follow the tutorial at the end).

**Requires Ubuntu 16.04 and ROS Kinetic.**

## Race world 
Race world is a Gazebo world that comes with the Jackal package. The Gwendolen agent simply moves to a coordinate in the map.

To run the race world simulation:
1. Copy the launch file `launch/jackal_world_with_rosbridge.launch` to `~/jackal_ws/src/jackal_simulator/jackal_gazebo/launch`
   * Make sure you either `source ~/jackal_ws/devel/setup.bash` everytime you wish to launch race world on a new terminal, or add it to your `~/.bashrc`
2. Copy the folder `simple_navigation_goals` to `~/jackal_ws/src/`
3. Recompile your catkin workspace by going to `~/jackal_ws/` and running `catkin_make`
4.  Copy the `src` folder to MCAPL root
5. Launch the race world in ros `roslaunch jackal_gazebo jackal_world_with_rosbridge.launch`
6. In Eclipse, go to `src/examples/gwendolen/ros/jackal/race`, right-click jackal.ail, select run as > run configurations, type run-AIL in the search box (should be there if MCAPL was installed correctly), and click on run
   * The robot will move to a specific coordinate in the world.
