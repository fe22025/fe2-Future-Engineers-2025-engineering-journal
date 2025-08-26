Engineering materials
====

This repository contains the source code developed for WRO Future Engineers category 2025, built using LEGO® SPIKE™ Prime hardware with additional sensors and modules. The vehicle combines modular LEGO motors and sensors with external hardware, allowing for autonomous navigation and real-time object detection.

The codebase is organized into the following main modules:

Motor Control Module – Interfaces with the SPIKE Prime motors to manage driving, turning, and speed regulation. </br> 

Ultrasonic Sensor Module – Reads distance values from the ultrasonic sensor and provides wall detection logic for safe navigation. </br> 

Camera Processing Module (OpenMV) – Uses the OpenMV camera to process visual data (e.g. color detection). The camera is connected via a custom-soldered adaptor for integration with the brain. </br>

Decision/Control Logic – Coordinates sensor inputs and issues motor commands, enabling autonomous behaviors such as turning on green/red and lap counting. </br>

Relation to Electromechanical Components: 
Motors → Controlled by the Motor Control Module for movement (forward, reverse, turning).
Ultrasonic Sensor → Feeds data to the navigation logic for collision prevention.
OpenMV Camera → Provides vision input used in higher-level decision making (colour detection)
Adaptor Board (soldered) → Serves as the interface between the OpenMV camera and the SPIKE Prime hub.


Build / Compile / Upload Process:
Programming Environment – The SPIKE Prime hub is programmed using MicroPython. The OpenMV camera is programmed using the OpenMV IDE.
Code Development – Python scripts for the SPIKE hub and OpenMV are written separately, but coordinated through serial communication and shared logic. 
Compilation/Upload –
SPIKE Prime code is uploaded via pybricks.
OpenMV code is uploaded using the OpenMV IDE. 
Execution – Once uploaded, the hub and camera modules run simultaneously, with the hub acting as the central controller that integrates motor and sensor data.

This repository contains all relevant code, organized into modules corresponding to the functions above, along with documentation on how to deploy and test the system.
