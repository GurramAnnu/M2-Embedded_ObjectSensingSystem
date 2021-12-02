
# Requirements
## Introduction
**The experimental setup is designed to detect object coming in the vision of ultrasonic sensor. An Arduino board is acting as embedded board which controls and monitors the desired operation. Ultrasonic sensor is having two eyes which is capable of sending pulse from one eye and if there is an object the generated pulse will get hit with the object and comes back as echo which is collected by the second eye.Radar is an system which detects objects by sending microwaves to calculate and know the distance, height, direction, or velocity of objects. The radar sends radio waves which come back after hitting off any object in their path with this method easily finding any object in the radar range.In these project, we've interfaced the Ultrasonic Sensor HC-SR04 with ATMEGA328 and LCD display. It sends an ultrasonic wave of a certain frequency which reflects back after hitting an object and also calculates the distance of object according to the time consumed for transmission and receiption of the waves.**

## Research
* The basic working principle of ultrasonic sensors is to emit sound waves of high frequencies which are inaudible for human ears, if these sound waves got hitten by any object they get reflected back as ECHO towards the sensor again. So we only needs to calculate the traveling time of both outgoing and incoming waves to it's origin after striking on the obstacle.
* The speed of sound is approximately 341 meters (1100 feet) per second in air. The ultrasonic sensor uses this information along with the time difference between sending and receiving the sound pulse to determine the distance to an object.

## Features, Hardware & software
#### _Features:_
      - High level signal is sent for 10us using Trigger  
      - Highly accurate
      - Detect a range of materials 
      - Specifications : Power Supply: +5V DC;  
                         Quiescent Current : <2mA;  
                         Working Current: 15mA;  
                         Effectual Angle: <15°;  
                         Ranging Distance : 2cm – 400 cm/1″ – 13ft; 
                         Resolution : 0.3 cm;  
                         Measuring Angle: 30 degree;  
                         Trigger Input Pulse width: 10uS;  
                         Dimension: 45mm x 20mm x 15mm
                         
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
 
