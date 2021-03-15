# orb_slam_3_ros  
Description:  
This repo contains both the standalong orb_slam3 module and ros wrapper for that orb_slam_3_ros.  

To install this package:  
1. Clone this package    
2. build with catkin_make   

<h4> To run the mono slam: </h4>    
roslaunch orb_slam_3_ros mono_euroc.launch  
Subscribed topic: /usb_cam/image_raw (sensor_msgs/Image)    

<h4> To run the mono inertial slam: </h4>    
roslaunch orb_slam_3_ros mono_inertial_euroc.launch  

Subscribed topic: /usb_cam/image_raw (sensor_msgs/Image)     
                  /imu (sensor_msgs/Imu)  
                  
According to the test on openvslam and orb_slam3 somehow orb_slam3 has showng bettern resutls when running visual slam processs.

Todo:
1. Integration of gridmap feature in this package such that when running slam 2d occupency grid map is generated in real time. Another package whih has tried smae thing which can be used and improved for better reliablility. https://github.com/skylook/ORB_SLAM2-gridmap 
2. SaveMap and LoadMap function implementation. https://github.com/UZ-SLAMLab/ORB_SLAM3/blob/master/include/System.h   
3. Fully ros compatible and removal of Pangolin viewer 
  3.1 pointcloud publisher   
  3.2 image publisher   
  3.3 dynamic reconfigurable parameters to change the orb_slam3 parameters in run time dynamically
( Note: Adding ros data publisher like sensor_msgs/Image or sensor_msgs/PointCluod2 is not complecated. Binding them with real data peroperly is. 
