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

## Prior Work
Online Edge Pulse, hard to collect dataset. Ours is better.

## Implementation
We use Arduino Nano 33 BLE Sense built in microphone and we connect a 8*8 Flex LED Panel to it. We use a 1200 mAH Lithium Battery as source. We decided to implement our mask like a sandwich. We embedded the Arduino and LED Panel in the outter mask, black color is desired for better light output. And inner mask is replaceble for healthy concern. The picture below is out implementation. The picture below is our mask.
## System Architecture
---
![flowchart](images/pipeline.png)

Our project are divided mainly in three parts. And we will discuss the function and technical approch in each part.
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
1. Recorded 30 seconds dataset for each keyword under both noisy and quiet environment. Similar to part1, we use PDM library to get rms value of voice and store all the value into a csv file.

2. Used scikit-learn library in Python to train a classifier to distinguish different keywords. 

3. Use micromlgen library to convert classifier into C code and implement it on Arduino. 

4. We test the keywords accuracy on Arduino, and choose "yes", "no", "happy", "sad" as our keywords. We need to avoid homophones for better result.

### Demo:

### Code Sample:
For generating data.

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


## Strength and Weakness

ML, dataset limited by arduino, connection, looks better.

## Future Direction
GUI, NLP(Rpi).

## Contribution


## Links

## Reference













## Hardware List / Budget
![budget](images/budget.png)











