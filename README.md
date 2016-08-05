STW HackWeek 2016 R2D2
======================


Startup
-------

R2D2 is based on Robot Operating System (ROS). To start him up, boot him up with the following steps:

1. Attach the Gigabyte computer module to a monitor using an HDMI or Mini DisplayPort cable. The monitor must be attached at bootup in order to start X-Windows propery, but it can be removed later.
2. Switch on the main power. This connects the 12V battery to the 120V AC inverter and the Roboclaw motor driver. A fan on the AC inverter should be audible once the power is switched on.
3. Turn on the Gigabyte computer module by pressing its power button. The computer will boot up quickly and automatically log in without a password.
4. Start up the ROS server by opening a terminal window and running `roscore`.
5. Start up the R2D2's ROS stack by using `cd ~/r2d2 ; source devel/setup.bash ; roslaunch launch/r2d2.launch`.
6. You may close the rtabmapviz window, if you do not want to use it.
7. Note the IP address by running `hostname -I` in a new terminal window.
8. Disconnect the monitor cable.


Control
-------

R2D2 is controlled remotely. He has a x11vnc server, which is capable of showing rviz and rtabmapviz windows. Note that these programs do not work with X11 remote access. Another option is to use the clickshare wireless video device along with a bluetooth keyboard and mouse.

You can run `rosrun telop_twist_keyboard telop_twist_keyboard.py` to get crude keyboard control over R2D2. 
