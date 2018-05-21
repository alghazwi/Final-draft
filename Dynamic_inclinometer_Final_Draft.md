---
layout: project (Final draft)
title: Dynamic Inclinometer
sponsor: Christopher Shultz
sponsor_url: http://www.hyster-yale.com/
document-date: 22 May 2018
---

## Project Objective

The objective of Hyster-Yale Group (HYG) project is to design a system that is able to measure the pitch and roll of a forklift, regardless of the vehicle's motion and orientation, while using HYG’s existing vehicle communication network by week 7 of spring term.

## Team

The project team members are

* Jose Garibay-Mendez
* Thien Ho
* Tixin Xue
* Mouaid Alghazwi

## Customer/Market Requirements

Use the client provided hardware; the Parker Impact Sensor(HYG's preferred sensor) and the CAN interface.

Reports on the inclination of the forklift. This will include the pitch(X,Y,Z) and the 3-axis rotation. The sensor should be able to update at a frequency of at least 1600Hz and provide a real time trace.

The system should have the ability to communicate with HYG's existing vehicle communication network. Information about the forklift's inclination must be relayed to the vehicle display panel via the Controller Area Network(CAN bus).

The system should work entirely automatically without any client interaction. The system should wake up when the forklift is powered and should continue to work until the forklift is powered off. Data will be stored in a .txt file for later revision if needed.

Accurate report of the pitch and roll angle measurement of the forklift. Range of the report accuracy should be positive and negative 25 degrees.

The budget of the system design to be 0 dollars. This will be made possible by using the client's hardware and software.

## Primary and Secondary client requirements

The table below classifies the client’s requirements according to the level of importance, primary requirements, secondary requirements and the performance matrix. Reports regarding the inclination of the forklift is the most important since that’s what the whole project is based on. The budget is the least important since the client provides the hardware and software. The team spends no money on the entire project.

![Primary and Secondary requiremetns table](https://github.com/alghazwi/Final-draft/blob/master/images/requirements.PNG)

## Design Challenges

One of the challenges is that, the sensor cannot be determined whether it has the capability to measure the pitch and roll of the forklift to a satisfactory degree until the capstone group has had a chance to work with the preferred sensor.

Another major challenge of the project will be designing a system that precisely and accurately reports accurate reading on the pitch and roll regardless of the vehicle’s motion. Centrifugal acceleration is likely to distort the readings of the sensor as the vehicle negotiates a corner.

## Outcomes

The team has developed a conceptual design that will be used for the system.

The diagram below shows the project architecture and design overview.It shows the overview of the steps that need to be accomplished in order to fulfill the requirements of the project. The figure below also summarizes the system design that will be implemented. It begins by using the client provided hardware and software in order to maintain the same communication network and topology as the one that HYG currently uses in their forklifts. The sensor that is used comprises of both an accelerometer and gyroscope which is capable of producing data to the six axes.

![Project Architecture](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/project_overview.png)

The following diagram shows analysis of all major subsystems. It also displays how to wire and program the sensor. The figure also shows the connections and interactions between the necessary components required to program and analyze data obtained from the sensor. The ifak CAN USB is used to view the CAN data that the sensor provides while the J-Link JTAG USB is used to program and debug the sensor. The ifak CAN USB is the preferred cable due to its compatibility with MATLAB. 

![Major Subsystems](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/analysis_subsystems.png)

The following diagram show the system level performance metrics and requirements matrix; The current design requirements and performance matrix.

![Performance requirements](https://github.com/alghazwi/Final-draft/blob/master/images/System%20level%20performance%20metrics%20and%20requirements%20matrix.png?raw=true)

The following diagram shows the accelerometer model. An accelerometer is an electromechanical device that is used to measure forces of acceleration. These forces may be static, like continuous gravitational forces or dynamic like vibrations and movements.Utilizing the model in the figure below, the resultant force, R, can be calculated using the following equation:
R=SQRT(〖Rx〗^2+〖Ry〗^2+〖Rz〗^2)


![Accelerometer Model](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/accelerometer_model.png)

The following diagram shows the gyroscope model.A gyroscope is a device comprising of a wheel or disc mounted so that it can rapidly spin about an axis which is itself free to alter in direction. The orientation of the axis is not affected by tilting of the mounting.An issue may arise with the three axes simulator to test the gyroscope due to some cable interference. This will however not hamper our development since the solution would be to alter and modify the code. If that doesn’t work, a one axis simulator will be designed and built. 

![Gyroscope Model](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/gyroscope_model.png)

The following photo shows the impact sensor. An issue may arise with learning how to use the sensor and it’s corresponding software and afterwards gathering and analyzing the data it produces. However, PSU has a lab that contains a three axes simulator and a centrifuge table. The team will first test the sensor to see if it is working properly and if the programmed code provides the desired output. Once the testing of the sensor is done and the team is satisfied that the sensor works properly and as planned, HYG will be contacted and we will request vehicle motion data as well as the corresponding data from the sensor. This data will then be analyzed and any required modifications to the code due to the introduction of the vehicles motion will be implemented. 
From the model below; Axz is the pitch angle and Ayz is the roll angle. These can be determined using the following equations:

tan⁡(Axz)=  Rx/Rz  =>atan⁡2(Rx,Rz)

tan⁡(Ayz)=  Ry/Rz=>atan2(Ry,Rz)

Combining the above two equations provides us with the resulting filter equation:

Angle=k*(Angle+GyroAngle*dt)+(1-k)*AccAngle

The true inclination angle will be determined by using a combination of the vehicles motion and the equations shown above. These calculations will be done using knowledge obtained from the dynamics class.

![Impact Sensor](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/impact_sensor.png)

The following photo shows the ifac usb.

![Impact Sensor](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/ifak_usb.png)

The following photo shows the jlink usb.

![Impact Sensor](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/jlink_usb.png)

The following shows the gant chart of how the tasks are planned to be completed.The Gantt chart describes the sequencing of tasks and time requirements. The actual task and the deliverable date may change. This variation will depend on the actual progress of the project.

![Gant chart](https://github.com/alghazwi/Final-draft/blob/d9f077a85337609a972ed507df7d9adbf71ab605/images/Gant%20chart.png)
