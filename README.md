## Table of Contents
- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Folder Layout](#folder-layout)
- [Contributors](#contributors)

# Overview
**Surge:** For Better Surgeries™. This is our university software engineering project that attempts to change the medical landscape around the world. The aim is to assist doctors during meticuluous operations for more efficient control and vision, this will be done by using a secure software combined with trained surgeons. This project will bridge the gap between modern technology and accessibility to all hospitals by being compact, accessible, and mobile. The assets of this tool are that it can perform surgeries faster by enhancing accuracy and ensuring cleaner operations, it provides more sterilized enviroment, brings the doctor important data and is overall a performance boost for the operator. Surge is ROS2 based, allowing the robot to be modular in nature.

## Benefits
**Surge** brings the following to the table:<br>
-Cost efficiency<br>
-Mobility<br>
-Real-time data analysis<br>
-Modularity<br>
and most importantly<br>
-Love<br>

## Tech Stack
**Languages:** C++, Python<br>
**Frameworks:** ROS2

## Folder Layout
The layout for this project will conform to the standard project layout of ROS2.<br>

## Contributors
Mohammed Najmaldeen<br>
Chera Ihsan<br>
Zeyineb Swara<br>
Savan Taher<br>
Mahmood Jihad<br>
Yahya Rubar<br>
Workspace: //brings all modules together into one environment, contains refreneces to all packages, build tool
- references all packages
- build tool settings
- extentions and other tools used in development
  
Bringup: //procss of launching entire system coordinately
- launch/
- config/
- CMakeLists.txt/
- package.xml/
  
Description: //describes what the robot looks like and how it's built
- CMakeLists.txt/
- package.xml/
- urdf/
- meshes/

Interface: //the language all nodes use to communicate
- CMakeLists.txt/
- package.xml/
- msg/
- action/
- srv/

Control: //the brains; recieves commands from UI then translates to instructions for motors, reads sensors, and updates diagnostics
- CMakeLists.txt/
- package.xml/
- src/
- config/
- include/
