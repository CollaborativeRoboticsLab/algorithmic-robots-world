# Algorithmic Robots World

This repo provides multiple containers to work with,

- Turtlebot4 Physical robots
- Simulation environment depicting a Mars surface
- Jupyter Notebook exploring basic concepts

[More information on Containers and Usage](./docs/containers.md)

## Install Docker

Follow the official instructions [here](https://docs.docker.com/engine/install/)

## Clone the repo

On the terminal run the following command to clone the repo

```sh
git clone https://github.com/CollaborativeRoboticsLab/algorithmic-robots-world.git
```

## Configure the parameters

Required environmental variables need to be in a `.env` file. An `example.env` file is available. Rename that file to `.env` and update the values as required.

[More information on Parameters](./docs/parameters.md)


## Start Simulation environment

```bash
cd algorithmic-robots-world
docker compose -f compose-simulation.yaml pull
xhost +local:root
docker compose -f compose-simulation.yaml up
```

## Start Physical robot environment

```bash
cd algorithmic-robots-world
docker compose -f compose-physical.yaml pull
xhost +local:root
docker compose -f compose-physical.yaml up
```

## Start Algorithmic Robotics Labs

```bash
cd algorithmic-robots-world
docker compose -f compose-jupyter.yaml pull
xhost +local:root
docker compose -f compose-jupyter.yaml up
```
