# ECE_M202A_MASK --- TEAM CL

This Project is for ECE M202A at UCLA

## Team Member:
Hongyi Chen

Rui Lin

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
1.Users can control the pattern and brightness of the LED panel. 

2.Users can control the on/off.

3.Users can monitor the battery usage.

4.Users can acquire the data from sensors, such as temperature, humidity, and the speed of walking.

### APP interface
1.Users can choose the pattern they like on the app.

2.Users can turn on or off the lightning functions.

### Rechargeable Battery System
1.Users can recharge the battery through micro-usb.

2.The Battery Indicator can show the 

3.The 1200 mAh Lithium Battery allows 2 hours usage.


## System Architecture

![flowchart](images/pipeline.png)












## Timeline

<b>Week 1-3</b>       <hr style="border:2px double ##1e90ff" width="400" size="2" />   <p>  Generate Idea</p>

<b>Week 4</b>         Proposal / Order Materials

<b>Week 5 </b>             Coding for Input and Output Pattern

<b>Week 6 </b>             Add Volume Detection function

<b>Week 7 </b>              First Prototyping and Test

<b>Week 8 </b>          Add BLE Interface and APP interface if the time allow

<b>Week 9 </b>              Final Test / Documentation

<b>Week 10 </b>             Demo

## Software 

Arduino IDE
Edge Pulse


## Hardware List / Budget
![budget](images/budget.png)











