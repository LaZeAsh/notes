---
title: "ROS Node"
draft: true
---

A node in ROS is responsible for a single, modular purpose, e.g. controlling the wheel motors or publishing sensor data from a laser range-finder. Each node can send and receive data from other nodes via topics, services, actions, or parameters

ROS 2, a single executable can contain one or more nodes

Referring to https://docs.ros.org/en/foxy/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Nodes/Understanding-ROS2-Nodes.html#the-ros-2-graph

A node in ROS 2 is like its own sub process that communicates with other processes exchanging only essential information.

An example of this is when I used to develop discord bots a shard would communicate with clusters but each cluster ran independently

## ros2 run

```bash
ros2 run turtlesim turtlesim_node
```

The package turtlesim has an executable turtlesim_node which will run after we use that command
## ros2 node list

