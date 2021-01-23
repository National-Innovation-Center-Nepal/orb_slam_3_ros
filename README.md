# orb_slam_3_ros
To run the mono slam:
roslaunch orb_slam_3_ros mono_euroc.launch
Subscribed topic: /usb_cam/image_raw : sensor_msgs/Image

To run the mono inertial slam:
roslaunch orb_slam_3_ros mono_inertial_euroc.launch

Subscribed topic: /usb_cam/image_raw : sensor_msgs/Image 
                  /imu : sensor_msgs/Imu
                  
According to the test on openvslam and orb_slam3 somehow orb_slam3 has showng bettern resutls when running visual slam processs.

Todo:
1. Integration of gridmap feature in this package such that when running slam 2d occupency grid map is generated in real time. Another package whih has tried smae thing which can be used and improved for better reliablility. https://github.com/skylook/ORB_SLAM2-gridmap 
2. SaveMap and LoadMap function implementation 
3. Fully ros compatible and removal of Pangolin viewer
