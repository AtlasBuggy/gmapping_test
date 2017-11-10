# gmapping_test
ROS Test for gmapping functionality
``rosrun gmapping_test lasercan_publisher`` runs the publisher which will start printing a count as well as publish fake laser scan data to /scan in sensor_msgs/LaserScan

``rostopic echo scan`` will print this data

``rosrun gmapping slam_gmapping scan:=scan`` will make gmapping try to map using this useless laserscan data (gmapping errors out but that should be just because the data is meaningless, should test with real laserscan data)
gmapping publishes data onto \map at nav_msgs/OccupancyGrid

