---
layout: page
title: Inter-Disciplinary Project
description: IDP during Master's at the Chair of Media Technology, Technical University of Munich
---

### SIMULINK auto-code generation for BeagleBoneBlack/Xenomai target

**At:** [Chair of Media Technology at Technische Universität München (TUM)](http://www.lmt.ei.tum.de/){:target="_blank"}

**Supervisor:** [Prof. Dr.-Ing. Eckehard Steinbach](http://www.lmt.ei.tum.de/en/team/team/eckehard-steinbach.html){:target="_blank"}

**Advisor:** [Rahul Chaudhari](http://www.lmt.ei.tum.de/en/team/alumni/rahul-chaudhari.html){:target="_blank"}

**Background:**

At the Institute for Media Technology, a first prototype of a portable multi-point haptic texture sensor and actuator system was developed.
This system consists of the following chain of components:
(multi-) sensor side –> digital processing –> (multi-) actuator side.

In the context of this system, there exist multiple alternatives for realizing the “digital processing” part.
Before the start of this project, two options were explored – the Arduino platform, and the RTAI/Linux/Desktop PC platform.
However, in both cases, one or the other shortcoming came across.
For example, in the case of Arduino, on-board memory for storing haptic texture data after recording or for display is very limited (of the order of kilobytes).
Moreover computational capacity is limited, so that complex signal processing (e.g. multichannel haptic signal compression) cannot be performed.
On the other hand, with the RTAI/Linux/Desktop PC platform, there is availability of many gigabytes of RAM, as well as high computational capacity.
However, the rate required for implementing SPI communication with multiple DAC chips is not supported by this
setup.
Moreover, this setup sacrifices on portability.
Presently, with these considerations, the BeagleBone Black (BBB) platform seems to be a very attractive solution for the following reasons – smartphone-like form factor, multi-channel ADC capabilities, a powerful TI Sitara(TM)
AM335x ARM Cortex(TM)-A8 Microprocessor coupled with 512 MB on-board RAM, and hardware SPI pins that can be used for driving DAC (actuator) side.

The figure below shows the sensor side of this system.
The haptuator box shown on the right acts as a haptic sensor as well as an actuator.
The sensor side has the current sensors mediating between the haptuator box and the BBB (as shown in the figure), whereas the actuator side has DAC chips followed by power amplifiers for driving the haptuator box.

![Beaglebone Black sensor actuator system](/res/images/bbb_sensor_actuator_system.png)

**Fig.:** *Picture of the multi-sensor/actuator system for multi-point haptic texture recording and playback (only the sensor side is shown here).
The Beaglebone Black on the left hand side samples and records, in realtime, multi-point haptic texture signals from the haptuator box on the right through a current-sensor circuit.*

This project, in combination to other related projects, completes this system prototype with respect to the software architecture, so that the system is ready end-to-end, and signal processing algorithms can be run between the sensor and the actuator sides.


**My Work:**

The Matlab/Simulink software provides a variety of standard signal processing algorithms implemented in the form of a Simulink-block library.
Program code can be automatically generated from a Simulink block diagram for specific target platforms.
At the Institute for Media Technology, a haptic texture codec has been developed and implemented in the form of a Simulink block diagram.
In order to deploy this codec between the sensor and actuator sides on the BBB, a Simulink interface needs to be
developed for auto-generating Xenomai code.
Moreover, so-called s-function interfaces (SIMULINK blocks) for the ADC and DAC sides need to be written.

From a higher level perspective, the steps taken in this project included:

* Studying the auto-code generation software architecture for the SIMULINK software through an example like RTAI/Linux which already provides a Simulink interface.
* Writing template MAKE files and SIMULINK tlc files for Xenomai code autogeneration.
* Collaborating with the executors of other related projects (for completing the system prototype as explained before) to write s-functions for the ADC and DAC sides, based on the Xenomai C-code coming from those projects.

