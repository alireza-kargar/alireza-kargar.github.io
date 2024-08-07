---
layout: post
title: Multi-modal autism screening system
description: A Multi-modal approach for comprehensive ASD screening
---

|![overview](https://alireza-kargar.github.io/assets/mmass/overview.png)|
|:-:|
|*system overview*|



Every 1 out of 160 children has Autism spectrum disorder; even though there is no treatment for ASD, early rehabilitation improves the patient's condition significantly. Autism has multiple symptoms that every child could experience with different severity. Although ASD can be diagnosed at six months, technical difficulties lead to time-consuming and expensive sessions due to complicated behavioral symptoms.
In recent years, technology-based methods for autism screening have been trending, and many researchers have developed apps, devices, and tools for ASD self-check or ASD rehabilitation. These tools usually screen autism based on only a specific feature or symptom that could be unreliable in many cases.

During my M.Sc. program in Advanced Robotics and Intelligent Systems Lab at the University of Tehran, I got acquainted with other researchers who have developed different ASD screening tools and devices over the past few years. For a mechatronics engineer who likes to create complicated systems, the challenge of integrating these various ASD screening tools looks compelling. Other than that, this system could be beneficial for children with ASD soon. So, we designed and developed a multi-modal system that screens based on multiple tools to cover the wide range of ASD symptoms. The multi-modal approach improves the accuracy and reliability of the ASD screening.

**System design:**

The central concept of designing an ASD screening system is to detect a related feature to a specific symptom. The general idea of how a feature relates to a symptom usually comes from ASD experts who experience ASD diagnosing sessions with children of different ages. We chose three more common symptoms of ASD: the deficit in social interactions, repetitive behavior, obsessive attention to detail, and hyperactivity of sensory inputs. The Roboparrot, the intelligent toy car, and the Lightwheel were selected accordingly.

**Roboparrot:**

Roboparrot is a parrot-like robot that was developed for human-robot interaction scenarios. Its previous versions were tested multiple times for ASD rehabilitation and screening. We developed Roboparrot 3.0 and made it compatible with ROS (Robotic Operating System).
Roboparrot can blink, open, and close its beak, move its body, and talk through a speaker.

|![ROS_diagram](https://alireza-kargar.github.io/assets/mmass/roboparrot_diagram.png)|
|:-:|
|*Roboparrot 3.0 diagram*|

**Intelligent toy car:**

The intelligent toy car is redesigned and developed to analyze the playing pattern of the children. The embedded sensors collect accelerations along the X, Y, and Z-axis and the number of wheel rotations for each timestamp.

|![ROS_diagram](https://alireza-kargar.github.io/assets/mmass/car_diagram.png)|
|:-:|
|*Intelligent toy car diagram*|

**Lightwheel:**

Lightwheel is developed for uncommon sensory input reactions based on the ASD experts' opinions. Children with ASD usually show an unusual interest in rotating objects, and they also tend to use bright lights. The Lightwheel tried to combine these two symptoms for ASD screening. The Lightwheel is  6 RGB LED strips placed in a circular pattern, and the periodic turning on and off makes the required sense of motion.

|![ROS_diagram](https://alireza-kargar.github.io/assets/mmass/lightwheel.png)|
|:-:|
|*Lightwheel and the system control board*|

**Intelligent ASD questionnaire:**

The intelligent questionnaire collects parents' observations on child behavior for a more comprehensive study. The questions were clustered and classified based on parameters like age, gender, and family background to enhance the performance of the questionnaire. Though this system does not analyze the child's behavior, collecting the parents' observations is proven effective.

**System integration:**

ROS plays a pivotal role in integrating all modules, so a ROS interface was developed for each module. Two cameras were provided to record the children's interactions with every module: one wide-angle fisheye lens camera on top of the system to ensure the recording of everything in the testing area, and one in front of the system to capture closer shots for facial expression analysis. These two cameras were handled by their ROS packages. Also, an action-based logging system was developed to synchronously record frames of each of the two cameras for each timestamp according to the system events (like the parrot's dialogues and the state of Lightwheel). The system could operate semi-autonomously or manually through a developed web interface to control the testing process and access its parameters, like the duration of each part.

The system assigns a unique ID for each user for privacy reasons, and the data-logging process proceeds based on that. Also, all recorded data, like videos, are saved locally, and after processing the raw videos and extracting essential features, the recorded videos are deleted.

After 15 to 20 minutes of interaction with the MMASS(multi-modal autism screening system), the intelligent toy car data, the video of Roboparrot child interaction, and the Lightwheel child interaction video were captured. Also, in the middle of this process, it was asked from the child's parents to fill out the questionnaire.

|![ROS_diagram](https://alireza-kargar.github.io/assets/mmass/ROS_diagram.png)|
|:-:|
|system ROS diagram|

**Data collection and processing:**

MMASS was tested on 16 children from 4 to 9 years old in one of the autism centers under the supervision of multiple ASD experts. All parents and legal guardians received proper paperwork beforehand to submit their consent, and all experiments were done in a familiar room for kids to ensure a less stressful process. Also, one of their parents or teachers could accompany them to reduce their anxiety.

The Intelligent toy car's data was analyzed with machine learning and signal processing methods, and the Roboparrot and Lightwheel footage was processed with image processing techniques to extract child interaction patterns. We used a pooling method to combine all the parts' results.

MMASS classifies autistic and non-autistic groups with 88% accuracy compared to 75% for the intelligent toy car, 86% for Roboparrot, and 88% for the Lightwheel. It also outperforms its tools and devices in sensitivity and accuracy of screening due to the multi-method approach. However, further tests are required to improve our data processing method and the system's accuracy, sensitivity, and specificity.


**Discussion:**

There are a few things we faced during our research that I would like to discuss:
- Due to COVID-19 restrictions, we did not have access to multiple ASD centers, so gathering more data to enhance the MMASS performance would be helpful.
- Analyzing child behaviors is a complicated task that we must simplify to reduce the parameters' space and complexity. First, The Roboparrot is a rather costly device that sometimes does not initiate an interaction with them, so maybe it's a good idea to replace it with an alternative. Second, the child should always be in the field of view of cameras to avoid any fault in the screening process.
- The MMASS is a collection of multiple tools placed in a pretty bulky cabinet. The transportation and the setup process could be troublesome, and a more lightweight system design is strongly suggested for future developments.

The MMASS project taught me many lessons, especially about how to effectively interact with children with ASD. This unique opportunity makes me see beyond the technicality of designing a system or writing stable software and understanding an engineering problem in the context of humans and their feelings.
We hope to publish our paper and open source all our works soon to elaborate more on our methods in the future.



