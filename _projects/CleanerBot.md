---
layout: post
title: Glass façade buildings cleaner Robot
description: Conceptual design of a cleaning robot platform
---

Skyscrapers and tall buildings have become more prevalent in our urban construction. Various facades and geometric designs are used in many iconic buildings, which cost significant budgets for cleaning and maintenance yearly. Different mechanical devices were developed to solve these issues and do the cleaning process. However, most of these mechanisms are used on flat surfaces, and their performance in overcoming obstacles is not usually acceptable.

|![CleanerBot_V1](https://alireza-kargar.github.io/assets/CleanerBot/CleanerBot_V1.png)|
|:-:|
|*The first glass façade cleaner Robot*|

Due to that, we decided to work in this area to reach a platform that could be used on different façades. At first, we designed and prototyped a facade-cleaning robot platform that could work on flat surfaces with short obstacles. In this prototype, the Robot moves down from the top of the building on the facade's surface with the help of a cable-driven connection and cleans the glass. Moreover, by using a crane implemented on the rooftop, it moved right and left.
Even though this prototype seemed practical, we were eager to design something more innovative to satisfy our academic desires, which led us to introduce a conceptual design and develop a semi-active seesaw-based facade-cleaning robot to overcome different shapes of obstacles and facade geometry compliantly.

|![Schematic_Design](https://alireza-kargar.github.io/assets/CleanerBot/CleanerBot_2.PNG)|
|:-:|
|*Implemented Seesaw mechanism prototype in different positions*|

To prove this concept, We designed a prototype and a test bench and then implemented a PD controller to adjust the applied force on the surface in semi-static situations. This system gets feedback from a rotational encoder attached to the main seesaw mechanism shaft and a load cell to show how much horizontal force is applied to the surface. Besides, a gyroscope has been connected to the mainframe just in case the system would return to its home position if it were out of balance. All were handled by an Arduino Mega 2560 selected to reduce cost and development time. Also, a graphical user interface was developed with Python so the system's status could be monitored at any time.

|![GUI](https://alireza-kargar.github.io/assets/CleanerBot/GUI.png)|
|:-:|
|*Glass façade cleaner Robot GUI*|

We tested the system on several shape surfaces, such as the stepped facade, S-shaped curve facade, slope facade, and flat surface facade, to understand its performance and find solutions for different scenarios to prevent potential problems as a bedrock for future improvements.

|![Testing_Platform](https://alireza-kargar.github.io/assets/CleanerBot/SurfacesTest.PNG)|
|:-:|
|*Testing the system on uneven surfaces*|