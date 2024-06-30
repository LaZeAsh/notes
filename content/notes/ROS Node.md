---
title: "ROS Node"
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

A command that hows you the list of running nodes, useful for when you want to keep track of nodes

## Remapping

`Remapping` - The ability to reassign default node properties to custom values

Remapping rules: https://design.ros2.org/articles/ros_command_line_arguments.html#name-remapping-rules

## ros2 node info

```shell
ros2 node info <node_name> # an example node_name is /my_turtle
```

This command returns a list of subscribers, publishers, services, and actions (aka the ROS graph connections that interact with that node)


