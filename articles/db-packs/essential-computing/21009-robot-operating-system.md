# Robot Operating System

The Robot Operating System (ROS) is an open-source middleware suite that lets robot software components discover each other, exchange messages, and share configuration data without knowing each other's internals. Despite its name, ROS is not an operating system. It is a layer of plumbing, tools, and reusable packages that runs on top of Linux (Ubuntu is the supported distribution; macOS and Windows 10 are experimental). It is written in C++, Python, and Lisp and released under the permissive BSD and Apache 2.0 licenses.

## What ROS actually provides

ROS gives a robot developer four capabilities:

1. **Hardware abstraction**, so the same code can address similar sensors and actuators from different vendors.
2. **Message passing between processes**, so independent programs exchange sensor data, commands, and state.
3. **Reusable packages** for common robotics tasks such as SLAM (simultaneous localization and mapping, building a map while tracking the robot's position inside it), navigation, motion planning, and perception.
4. **A build system and command-line tools** for assembling, launching, and debugging these components.

ROS is not a real-time operating system (an OS that guarantees a task finishes within a strict deadline). Low-latency control is possible only by integrating ROS with separate real-time code. This limitation is the main reason ROS 2 exists.

## The computation graph

ROS software is organised as a graph. Each running program is a **node** with a unique name. Nodes communicate through three mechanisms:

- **Topics** are named buses for continuous streams. A node publishes to a topic when it produces data and subscribes when it consumes it. The publish/subscribe model is anonymous, so publishers do not know who is listening. Sensor streams and motor commands travel over topics.
- **Services** are request-reply calls for discrete actions with a clear start and end, such as capturing a single image.
- **The parameter server** is a shared dictionary of slow-changing values, such as a robot's wheel radius, that any node can read.

A process called the **ROS 1 Master** acts as a name service. Nodes register with it on startup, and the master tells them how to find each other so they can talk peer-to-peer afterwards. This decentralised layout fits robots, which are themselves small networks of processors, and lets heavy computation be offloaded to a separate computer.

## Core tools

A few tools ship with most ROS installations and shape daily development. **rviz** is a 3D visualiser for robot models, environments, and live sensor data, with robots described in URDF, an XML format. **rosbag** records topic traffic to a file called a bag and plays it back later, which is the standard way to capture datasets for offline testing. **roslaunch** starts many nodes at once, including on remote machines, from a single XML file. **catkin** was the ROS 1 build system (based on CMake); ROS 2 replaced it with `colcon`, though catkin is still maintained for legacy code. **rosbash** adds shell commands like `roscd` and `rosls` that navigate by package name rather than file path.

## Notable packages

The ROS ecosystem is largely defined by its packages. Widely used ones include `slam_toolbox`, `gmapping`, `cartographer`, and `amcl` (adaptive Monte-Carlo localisation) for mapping and localisation; `navigation` for planar mobile-robot movement; `MoveIt!` for manipulator motion planning, built on the Open Motion Planning Library (OMPL); `vision_opencv` for bridging OpenCV; `tf2` for tracking and transforming coordinate frames; and `gazebo_ros_pkgs` for integrating the Gazebo simulator. Each solves a problem common enough that almost every serious robot reuses it.

## History

ROS began in 2007 at Stanford, where PhD students Eric Berger and Keenan Wyrobek, working in Ken Salisbury's robotics lab, wanted a common baseline for robotics research. Early code drew on the switchyard framework that Morgan Quigley had built for the Stanford AI Robot (STAIR). Scott Hassan, founder of Willow Garage, shared their "Linux for robotics" vision and hired them; the first ROS commit was pushed to SourceForge on 7 November 2007.

Willow Garage then drove the project through 2013. The PR2 became the reference hardware, and in March 2010 Willow Garage released Box Turtle, the first official ROS distribution (a tested, versioned bundle of packages for public installation). Eleven PR2s went to universities including MIT, Stanford, UC Berkeley, Freiburg, KU Leuven, and the University of Tokyo, seeding a global user base. Willow Garage created the Open Source Robotics Foundation (OSRF) in 2012; OSRF renamed itself Open Robotics in 2017 and took over maintenance in 2013 after Willow Garage was absorbed into Suitable Technologies. Under Open Robotics, ROS reached every continent, ran aboard NASA's Robonaut 2 on the International Space Station (September 2014), was ported to Windows by Microsoft in 2018, and was extended into AWS RoboMaker the same year.

## ROS 2

ROS 1's lack of real-time support made it unsuitable for safety-critical and embedded use. ROS 2, announced at ROSCon 2014 with first commits in February 2015 and the first distribution Ardent Apalone released 8 December 2017, replaces the custom master with DDS (Data Distribution Service, an industrial standard for real-time publish-subscribe communication) for discovery and transport, enabling real-time code, embedded targets, and a wider range of platforms.

ROS 2 ships a new distribution each May, aligned with Ubuntu LTS (Long-Term Support) releases. LTS versions on even-numbered years are supported for five years; non-LTS releases get about 1.5 years. As of May 2026 the latest release is Lyrical Luth; the last ROS 1 distribution, Noetic Ninjemys (May 2020), reached end of life in May 2025. ROS 1 and ROS 2 can coexist on the same machine, which matters because much production and research code still targets ROS 1.

## Extending ROS

Two notable extensions push ROS into adjacent domains. **ROS-Industrial**, founded in January 2012, ports ROS capabilities to factory robots from ABB, Fanuc, Motoman, and Universal Robots, maintained by regional consortia in the Americas, Europe, and Asia-Pacific. **Space ROS**, announced in November 2020, is a NASA and Blue Origin effort now led by PickNik and the Open Source Robotics Foundation that builds a ROS 2 derivative compliant with aerospace safety standards such as DO-178C.
