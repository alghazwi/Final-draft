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

## Design Challenges

One of the challenges is that, the sensor cannot be determined whether it has the capability to measure the pitch and roll of the forklift to a satisfactory degree until the capstone group has had a chance to work with the preferred sensor.

Another major challenge of the project will be designing a system that precisely and accurately reports accurate reading on the pitch and roll regardless of the vehicle’s motion. Centrifugal acceleration is likely to distort the readings of the sensor as the vehicle negotiates a corner.

## Outcomes

The team has developed a conceptual design that will be used for the system.

The following diagram shows the project architecture and design overview.

![Project Architecture](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/project_overview.png)

The following diagram shows analysis of all major subsystems.

![Major Subsystems](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/analysis_subsystems.png)

The following diagram show the system level performance metrics and requirements matrix

![Major Subsystems](https://github.com/alghazwi/Final-draft/blob/master/images/System%20level%20performance%20metrics%20and%20requirements%20matrix.png?raw=true)

The following diagram shows the accelerometer model.

![Accelerometer Model](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/accelerometer_model.png)

The following diagram shows the gyroscope model.

![Gyroscope Model](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/gyroscope_model.png)

The following photo shows the impact sensor.

![Impact Sensor](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/impact_sensor.png)

The following photo shows the ifac usb.

![Impact Sensor](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/ifak_usb.png)

The following photo shows the jlink usb.

![Impact Sensor](https://github.com/alghazwi/Dynamic-inclinometer/blob/master/Dynamic/images/jlink_usb.png)

The following shows the gant chart of how the tasks are planned to be completed.

![Impact Sensor](https://github.com/alghazwi/Final-draft/blob/d9f077a85337609a972ed507df7d9adbf71ab605/images/Gant%20chart.png)
