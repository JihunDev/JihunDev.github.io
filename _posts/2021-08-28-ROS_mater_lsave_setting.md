---
author: Jihun Kim
categories:
- Software
- ROS
comments: true
date: 2021-08-28 00:00:00 +0000
math: false
mermaid: false
pin: false
tags:
- ROS
- Network
- Robotics
- Setup
title: ROS Mater, Slave Setting
---

---

# Configuration the .bashrc File 

## Primary

~/.bashrc

```bash
export ROS_MASTER_URI=http://localhost:11311
export ROS_HOSTNAME={PrimaryName}
export ROS_IP={PrimaryIp}
```

##  Secondary

~/.bashrc

```bash
export ROS_MARTER_URI=http://{PrimaryIp}:11311
export ROS_HOSTNAME={SecondaryName}
export ROS_IP={SecondaryIp}
```

## Apply .bashrc

```bash
$ source ~/.bashrc
```

# Configuration the /etc/hosts File
- Same setting for Primary and Secondary

```bash
<PrimaryIP> <PrimaryName>
<SecondaryIP> <SecondaryName>
```

# Reference

    [Wiki](http://wiki.ros.org/ROS/Tutorials/MultipleMachines)