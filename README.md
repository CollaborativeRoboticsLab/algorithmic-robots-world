# Algorithmic Robots World

This repo provides multiple containers to work with Turtlebot4 Robots in [DiscoveryServer Mode](https://turtlebot.github.io/turtlebot4-user-manual/setup/discovery_server.html). 

This pacakge provides and utilizes following containers

- **Turtlebot4-Discovery**          
    Provides the discovery service for the simulation

- **Algorithmic-Robots-Mars-Surface-Simulation**         
    Provides the Unreal based simulation environment

- **Turtlebot4-Rviz**   
    Provides rviz tools to interact with both simulation and physical robots

- **Turtlebot4-workspace**  
    Provides a web browser based workspace that can be used to test code on both simulation and physical robots

- **Algorithmic-robots-labs**
    Provides a Jupyter notebooks based workspace to explore mathematical concepts surrounding robotics


## Install Docker

Follow the official instructions [here](https://docs.docker.com/engine/install/)

## Clone the repo

On the terminal run the following command to clone the repo

```sh
git clone https://github.com/CollaborativeRoboticsLab/algorithmic-robots-world.git
```

Required environmental variable need to be in a `.env` file. An `example.env` file is available. Rename that file to `.env` and update the values as required. 


## Start Simulation environment

```bash
cd algorithmic-robots-world
docker compose pull
docker compose up
```

## Start Physical robot environment

```bash
cd algorithmic-robots-world
docker compose -f compose-physical.yaml pull
docker compose -f compose-physical.yaml up
```

## Start Algorithmic Robotics Labs

```bash
cd algorithmic-robots-world
docker compose -f compose-teaching.yaml pull
docker compose -f compose-teaching.yaml up
```