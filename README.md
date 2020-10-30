# ECE_M202A_MASK

This Project is for ECE M202A at UCLA

## Overview

A mask doesn’t have to hide the smiling while protecting people from possible COVID-19 infection.The Voice-Activated LED facial mask is not only a PPE, but also a wearable IoT device which implements BLE and various sensors. It can protect the user from viruses while mimicking someone talking or smiling even when their mouth is hidden behind the protective cloth. 

The team is going to implement machine learning to build a system that can recognize when a particular sound is happening—a task known as audio classification. The system is able to recognize the sound of crying and smiling, even in the presence of other background noise. The team will collect audio data from built-in microphones, use signal processing to extract the most important information, and train a deep neural network that can transfer sound to words. Finally, deploy the system to the Arduino Nano 33 BLE SENSE to control the LED panel.

## Goals

The Voice-Activated LED Facial Mask is designed to achieve three functions at the current stage. The team is going to add or delete functions based on the team’s timetable and progress.

### Voice Recognition 
The mask is able to detect the word and specific tones through machine learning, The LED will output different patterns such as smiling and crying, which depends on the keyword.
### Volume Amplitude Recognition
The mask can adjust the mouth-opening pattern by voice volume.
### BLE Interface
Users can control the pattern and brightness of the LED panel. 
Users can control the on/off.
Users can monitor the battery usage.
Users can acquire the data from sensors, such as temperature, humidity, and the speed of walking.
### APP interface
Users can choose the pattern they like on the app.
Users can turn on or off the lightning functions.
Rechargeable Battery System
Users can recharge the battery through micro-usb.
The Battery Indicator can show the 
The 1200 mAh Lithium Battery allows 2 hours usage.


## System Architecture

![flowchart](images/pipeline.png)












## Timeline

Week 1-3            Generate Idea
Week 4               Proposal / Order Materials
Week 5               Coding for Input and Output Pattern
Week 6               Add Volume Detection function
Week 7               First Prototyping and Test
Week 8               Add BLE Interface and APP interface if the time allow
Week 9              Final Test / Documentation
Week 10            Demo

## Software 

Arduino IDE
Edge Pulse


## Hardware List / Budget
![budget](images/budget.PNG)











