# ECE_M202A_MASK --- TEAM CL

This Project is for ECE M202A at UCLA

## Team Member:
Hongyi Chen

Rui Lin

## Overview
---
### Motivation
Under the tough COVID-19 pandemic, thousands of people lost their lives and lots of hospitals' ICU are hitting capacity. However, there are a lot of people still not wearing masks. We want to do something to encourage everyone to wear a mask which helps stop spreading of virus. A mask doesn’t have to hide the smiling while protecting people from possible COVID-19 infection. Thus, the Voice-Activated LED facial mask we built is not only a PPE, but also a wearable IoT device which implements BLE and various sensors. It can protect users from virus while mimicking their talking or smiling even when their mouth is hidden behind the protective cloth. 


### Goals

Build a mask which is able to detect voice volume, recognize the sound of crying and smiling under a noisy environment, and output different patterns on LED.  

### Hardware List
1. Arduino Nano 33 BLE Sense

2. 8*8 Flex LED Panel

3. 1200 mAH Lithium Battery

4. Battery Charger

5. Facial Mask (desire black)

## System Architecture
---
![flowchart](images/pipeline.png)

## Part 1: Volume Amplitude Detection and Output  
---
### Function:
The mask can adjust the mouth-opening pattern by voice volume. We extract the peak rms value of sound for a certain period, and we set certain threshold for loud and silent situations. 

### Demo:
Video:

### Sample Code

## Part2: Keyword Reconginzer and Print Emoji
---
### Approach Process and Method
1. Recorded dataset for our keywords and noise under different scenarios.

2. Used scikit-learn library in Python to train a classifier to distinguish different keywords.

3. Choose words with higher accuracy and avoid homophones to make sure the robustness.

4. Use micromlgen library to convert classifie into C code and implement it on Arduino

### Demo:

### Code Sample:


## Part3: Keyword Recognizer and Print Characters
#### BLE Interface
1.Users can control the pattern and brightness of the LED panel. 

2.Users can control the on/off.

3.Users can monitor the battery usage.

4.Users can acquire the data from sensors, such as temperature, humidity, and the speed of walking.

#### APP interface
1.Users can choose the pattern they like on the app.

2.Users can turn on or off the lightning functions.

#### Rechargeable Battery System
1.Users can recharge the battery through micro-usb.

2.The Battery Indicator can show the 

3.The 1200 mAh Lithium Battery allows 2 hours usage.


















## Hardware List / Budget
![budget](images/budget.png)











