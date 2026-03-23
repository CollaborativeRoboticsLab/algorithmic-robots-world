# Parameters

## SIM_ROS_DOMAIN_ID (default : 0)

This parameter helps to isolate the simulation environment from other laptops and similar environments in the same network. If the simulation shows unexpected behaviours and movements, this could be because there is another system with same SIM_ROS_DOMAIN_ID. Make sure to keep this unique.


## ROBOT_ROS_DOMAIN_ID (default : 0)

This parameter helps to isolate the robot and laptop environment from other laptops and similar robots in the same network. If the robot shows unexpected behaviours and movements, this could be because there is another system with same ROBOT_ROS_DOMAIN_ID. Make sure to keep this unique.


## ROBOT_ROS_DISCOVERY_SERVER=10.42.0.1:11811

This parameter indicates where the ros2 fastdds discovery server is. In the context of these labs, the fastdds discovery server lives in each robot. When you pick a robot, find the IP address of that robot and update this parameter. Keep the port as 11811.