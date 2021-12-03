   # _PROJECT REPORT_
# Requirements:
## Introduction
  * With the increasing demand for autonomous projects, the use of sensors is increasing. Sensors are sophisticated devices that convert the physical parameter (for example: temperature, pressure, humidity, speed, etc.) into a signal which can be measured electrically. 
  * In Industrial applications, ultrasonic sensors can be used to solve even the most complex tasks involving object detection or level measurement with millimeter precision,because their measuring method works reliably under almost all conditions.
  * In these project, we've interfaced the Ultrasonic Sensor HC-SR04 with ATMEGA328 and LCD display. It sends an ultrasonic wave of a certain frequency which reflects back after hitting an object and also calculates the distance of object according to the time consumed for transmission and receiption of the waves.

## Research
![Description](Link to Pic)
* The basic working principle of ultrasonic sensors is to emit sound waves of high frequencies which are inaudible for human ears, if these sound waves got hitten by any object they get reflected back as ECHO towards the sensor again. So we only needs to calculate the traveling time of both outgoing and incoming waves to it's origin after striking on the obstacle.
* The speed of sound is approximately 341 meters (1100 feet) per second in air. The ultrasonic sensor uses this information along with the time difference between sending and receiving the sound pulse to determine the distance to an object.

## Features, Hardware & software
#### _Features:_
      - High level signal is sent for 10us using Trigger  
      - Highly accurate
      - Detect a range of materials 
      - Specifications : Power Supply: +5V DC;  Quiescent Current : <2mA;  Working Current: 15mA;  Effectual Angle: <15°;  Ranging Distance : 2cm – 400 cm/1″ – 13ft; 
        Resolution : 0.3 cm;  Measuring Angle: 30 degree;  Trigger Input Pulse width: 10uS;  Dimension: 45mm x 20mm x 15mm
 
  #### _Hardware:_
    1] ATmega328:
       - ATmega328 is commonly used in many projects and autonomous systems where a simple, low-powered, low-cost micro-controller is needed
       - Perhaps the most common implementation of this chip is on the popular Arduino development platform.
     
    2] LCD Module:
       - LCD modules are very commonly used in most embedded projects, the reason being its cheap price, availability, programmer 
       friendly and available educational resources.
     
    3] HC-SR04:
       - HC-SR04 Ultrasonic sensor is used to detect the obstacle.
     
 #### _Software:_
    1] SimulIDE:
       - SimulIDE provides AVR, Arduino and PIC microcontrollers that can be accessed just like other components. 
       - Features like gpsim and simavr allow you to use PIC and AVR microcontrollers, respectively.
     
    2] WinAVR:
       - WinAVR is a suite of executable, open source software development tools for the Atmel AVR series of RISC microprocessors
        hosted on the Windows platform. It includes the GNU GCC compiler for C and C++.
 
![Description](Link to Pic)
     
## Defining Our System
    The module works on the natural phenomenon of ECHO of sound. A pulse is sent for about 10us to trigger the module. After which
    the module automatically sends 8 cycles of 40 KHz ultrasound signal and checks its echo. The signal after striking with an
    obstacle returns back and is captured by the receiver. Thus the distance of the obstacle from the sensor is simply calculated
    by the formula given as,

                                                  Distance= (time x speed)/2.
   
    Here we have divided the product of speed and time by 2 because the time is the total time it took to reach the obstacle and 
    return back. Thus the time to reach obstacle is just half the total time taken.
## SWOT ANALYSIS
![SWOT-Sample](Link to Pic)

### _Strength_
    * The sensors can measure distances form 2 to 400cm with an accuracy of 3mm.
    * Not affected by color or transparency of objects
    * Can be used in dark environments
    * Not highly affected by dust, dirt, or high-moisture environments
    * The distance to an obstacle can be measured with the low cost ultrasonic sensor. 
### _Weakness_   
    * The module can't work in a vacuum
    * Sensing accuracy affected by soft materials
    * Although the sensor performance and reliability is very good but still it is not suited for every application. 
    * It has a tendency to assimilate sound vitality and focuses on low thickness, these materials may be hard to sense at long range.
### _Opportunity_
    * In many applications like vehicle control, medical applications, robotic movement control, etc.; detection and distance 
      measurement of an object is used.
### _Threats_
    * Limited testing distance
    * Chances of inaccurate readings
    * Inflexible scanning methods.
    
    
# 4W&#39;s and 1&#39;H

## Who:

**The importance of the project is to detect and calculate accurate distance from any obstacle that we want to measure. Ultrasonic sensors are used primarily as proximity sensors. They can be found in automobile self-parking technology, medical applications and anti-collision safety systems**

## What:

**I have made a setup based on a microcontroller in which object detection and real time distance is sensed by an ultrasonic sensor and displays measured distance on an LCD display.**

## When:

**This will be useful to user when they need assistance in dark light and whenever we want to measure the particular distance from the moving object.**

## Where:

**It measures accurate distance using a non-contact technology.**

## How:

**Ultrasonic sensors generate high frequency sound waves and evaluate the echo which is received back by the sensor if obstacle detected. Sensors calculate the time interval between sending the signal and receiving the echo to determine the distance to an object.**

# Detail requirements
## High Level Requirements:

| ID | Description | Status |
| -- | ----------- | ----------- |
| HLR1 | Interfacing Ultrasonic Sensor with controller  | Implemented |
| HLR2 | Interfacing LCD display with controller   | Implemented |
| HLR3 | Installing required softwares on the PC/Laptop | implemented |


##  Low level Requirements:
| ID | Description | Status | 
| -- | ----------- | ----------- |
| LLR1 | Setting the range upto 80 cm | Implemented |
| LLR2 | The high-level signal is sent to 10 microseconds using Trigger | Implemented |




#   Block  Diagram of the System:


![ultra](https://github.com/Nayan349/M2-Embedded_ObstacleDetectionSystem/blob/3e72a26d8ed20238021862cc721036d6dae13328/2_Design/Block%20Diagram%20Of%20The%20System/Block%20Diagram.jpg)



## Behavioural Diagram :


![Flow Chart](https://github.com/Nayan349/M2-Embedded_ObstacleDetectionSystem/blob/38c589fc3e8156c4df0a41095926484a73e74dc6/2_Design/Behavioural%20Diagrams/Flow%20Chart.png)



# TEST PLAN
## Table no: High level test plan
| Test ID |           Description       |      Exp I/P    |    Exp O/P   |   Actual Out  |   Type Of Test |
| --------| --------------------------- | --------------- | ------------ | ------------- | -------------- |
|  HL01   | Sensor Working | Obstacle  |  Obstacle Detected    |   As Expected | Requirement Based |
|  HL02   |      High accuracy     |  Object in the range  |    Accurate distance from object on Display   |   As Expected | Scenario based |
|  HL03   | Measuring time lapses between the sending and receiving of the ultrasonic pulse | Object in the range | Display   |   As Expected | Requirement Based |

### Table no: Low level test plan
| Test ID |           Description       |      Exp I/P    |    Exp O/P   |   Actual Out  |   Type Of Test |
| --------| --------------------------- | --------------- | ------------ | ------------- | -------------- |
|  LL01   | Detection of clear objects | Obstacle | Display  | As Expected   | Scenario based |
|  LL02   | Provide multiple range measurements per second | Moving Obstacle | Display   | As Expected  | Requirement Based |



# Communication Protocols
## Wired
#### In this project we use UART communication protocol.
### UART  - TX & RX (2 devices)
* 2 Wire
* Individual clocks used by the both parties
* Standard speed (9600, 115200) - Baud rate
* Parity

## Factors to decide on which communication prototocol to select
### * Frequency :
We need 2oKHz frequency for this project because of this UART is suitable for this model.
### * Data throughput
### * Number of pins available :
There are two pins are avaiable.
#### [1] TX (Pin no 3)
#### [2] RX (Pin no 2).
TX and RX pins we need to display our result .



# Conclusion
The objective of the project was to design and implement an obstacle detection system. The device described here can detect the 
target and calculate the distance of the target. The Obstacle Detection System is a low cost, low a simple device for distance 
measurement. The device calculates the distance with suitable accuracy and resolution. It is a handy system for non-contact 
measurement of distance. The device has its application in many fields. It can be used in car backing system, automation and 
robotics, detecting the depth of the snow, water level of the tank, production line. This device will also have its application in civil 
and mechanical field for precise and small measurements.
For calculating the distance using this device, the obstacle whose distance is to be measured should always be perpendicular 
to the plane of propagation of the ultrasonic waves. Hence the orientation of the target is a limitation of this system. The ultrasonic 
detection range also depends on the size and position of the target. The bigger is the obstacle, stronger will be the reflected signal 
and more accurate will be the distance calculated. Hence the ultrasonic distance meter is an extremely useful device.
