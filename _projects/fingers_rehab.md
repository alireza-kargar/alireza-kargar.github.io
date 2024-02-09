---
layout: post
title: Fingers rehabilitation device
description: Rehabilitation device for fingers suffering from spasm
---

Spasticity is one of the most common challenging disorders after nerve damage. Due to challenges that exist over time in the treatment process, some engineers have decided to build rehabilitation systems. In this project, we designed and implemented a device inspired by cylindrical tools and pieces commonly used in rehabilitation and physiotherapy centers. This device uses a structure consisting of two rows of rollers connected by three springs with different stiffnesses to adjust pressure and perform rehabilitation operations; also, three rollers exist in each row. These rows are installed in a module called "the Hand Holder." At the beginning of the rehabilitation operations, the patient's hand is placed between two rows of rollers in the Hand Holder. Then, it moves periodically back and forth in a linear mechanism to perform extension and flexion exercises.


|![FRD](https://alireza-kargar.github.io/assets/FRD/frd_1.png)|
|:-:|
|*Fingers Rehabilitation device*|

The electronic part of the rehabilitation system is implemented on the Arduino Mega microcontroller board. This section includes the following two subsections:

**Implementation of extension and flexion exercises:** The system's main task is to perform extension and flexion operations for the hands of adult patients of different sizes. When therapists open and close patients' fingers, they apply a relatively constant force to them, opening and closing almost at a constant speed. So, after the patient's fingers are placed in the Hand Holder, the speed of the motor and the number of exercises are determined by the user. Then, the rehabilitation operation of opening and bending the fingers begins with the device. The patient ID number, the motor's initial speed, and the device's training number are shown on the device's graphical LCD. Also, when a technical fault occurs in the electronic part of the device, the problem and solution to fix it are displayed on the screen.
**Data collection:** In the device, data collection is done by a Time-of-Flight (ToF) distance sensor. The distance of a marker mounted on the Hand Holder to the sensor is recorded and stored in the memory card. 


|![Diagram](https://alireza-kargar.github.io/assets/FRD/diagram.png)|
|:---:|
|*block diagram of the electronic part of the rehabilitation device*|

The following safety features have been applied in the rehabilitation system:

An emergency stop push button is used in the system for the therapist to disable the device when observing any abnormal event. A key lock is placed in the rehabilitation system to prevent non-specialists from using it (such as children and people who cannot access the device). The user can lock and deactivate the system after rehabilitation sessions. In case any abnormal load is applied to the system and the device's speed increases due to a technical fault, the Hand Holder will automatically go to the predetermined destination specified by a micro switch with a roller lever and stop. The distance between the place where the patient's wrist is fixed and the starting point of the Hand Holder's movement is 2cm (more than the thickness of an adult's hand with an X-large size). Therefore, if the patient's hand gets out of the Hand Holder while moving, the Hand Holder will not cause any damage to the hand when returning to the starting point. All surfaces in contact with the patient's forearm, wrist, and hand are covered with foam and leather layers to ensure patient compatibility with the device during rehabilitation.
