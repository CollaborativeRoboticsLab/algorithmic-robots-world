# Parameters

## SIM_ROS_DOMAIN_ID (default : 0, range 0-255)

This parameter helps to isolate the simulation environment from other laptops and similar environments in the same network. This only need to be set on the laptop. If the simulation shows unexpected behaviours and movements, this could be because there is another laptop with same SIM_ROS_DOMAIN_ID in the network. Make sure to keep this unique by talking to fellow students.


## ROBOT_ROS_DOMAIN_ID (default : 0, range 0-255)

This parameter helps to isolate the robot and laptop environment from other laptops and similar robots in the same network. This value has been already set in the robot and needs to be set only on the connecting laptop. If the robot shows unexpected behaviours and movements, this could be because there is another laptop with same ROBOT_ROS_DOMAIN_ID. Make sure to match this to the value on the robot.

### Finding the ROS_DOMAIN_ID on the robot

Generally this is matched to the robot's name. If the robot is `TBOT4-001`, the ROS_DOMAIN_ID is `1`. Otherway to find out is by logging into the robot via SSH and running the following command,

```bash
echo $ROS_DOMAIN_ID
```


## ROBOT_ROS_DISCOVERY_SERVER (Default: 10.42.0.1:11811)

This parameter indicates where the ros2 fastdds discovery server is. In the context of these labs, the fastdds discovery server lives in each robot. When you pick a robot, find the IP address of that robot and update this parameter. Keep the port as 11811. 

### Finding the IP address

Each robot has a small display near its Power button. That shows the IP address. Other option is to connect to the Rpi's Ethernet via Ethernet cable and connect to the robot. Set remote machine's IP address 192.168.185.10, NetMask 255.255.255.0 and use SSH to connect. Use following command. Password is `turtlebot4`