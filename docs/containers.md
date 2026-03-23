# Containers and Usage

This repo uses following containers

- **Turtlebot4-workspace**
    - link [ghcr.io/collaborativeroboticslab/turtlebot4-workspace:jazzy](https://github.com/CollaborativeRoboticsLab/turtlebot4-docker/pkgs/container/turtlebot4-workspace)
    - Provides a web browser based workspace that can be used to test code on both simulation and physical robots. Contains ROS2 Jazzy Desktop with GUI tools for debugging. Use this to do development work

- **Algorithmic-Robots-Mars-Surface**   
    - link [ghcr.io/collaborativeroboticslab/algorithmic-robots-mars-surface:jazzy](https://github.com/CollaborativeRoboticsLab/algorithmic-robots-world/pkgs/container/algorithmic-robots-mars-surface)     
    - Provides the Unreal based simulation environment to work with when Physical robots are inaccessible.

- **Algorithmic-Robots-Labs**
    - link [ghcr.io/collaborativeroboticslab/algorithmic-robots-labs:latest](https://github.com/CollaborativeRoboticsLab/algorithmic-robots-labs/pkgs/container/algorithmic-robots-labs)
    - Provides a Jupyter notebooks based workspace to explore mathematical concepts surrounding robotics


## Simulation System

This system can be started with `compose-simulation.yaml` file. This starts a simulation environment and a browser based vs-code environment for experiments using following containers

- `Algorithmic-Robots-Mars-Surface` container
- `Turtlebot4-workspace` container

Update the following environment variables to isolate the ROS environment

```bash
SIM_ROS_DOMAIN_ID=0
```

Use the following commands to start the system

```bash
cd algorithmic-robots-world
docker compose -f compose-simulation.yaml pull
xhost +local:root
docker compose -f compose-simulation.yaml up
```

## Start Physical robot environment

This system can be started with `compose-physical.yaml` file. This starts a browser based vs-code environment for experiments and connects with the Discovery server in the Turtlebot4 robot. It uses following containers

- `Turtlebot4-workspace` container

Update the following environment variables to isolate the ROS environment

```bash
ROBOT_ROS_DOMAIN_ID=0
ROBOT_ROS_DISCOVERY_SERVER=10.42.0.1:11811
```

Use the following commands to start the system.

```bash
cd algorithmic-robots-world
docker compose -f compose-physical.yaml pull
xhost +local:root
docker compose -f compose-physical.yaml up
```

## Start Algorithmic Robotics Labs

This system can be started with `compose-jupyter.yaml` file. This starts a browser based jupyter environment for tutorial activities. It uses following container

- `Algorithmic-Robots-Labs` container

```bash
cd algorithmic-robots-world
docker compose -f compose-jupyter.yaml pull
xhost +local:root
docker compose -f compose-jupyter.yaml up
```


