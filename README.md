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
[![Volume Detection](http://img.youtube.com/vi/ARSoRdHVBX4/0.jpg)](http://www.youtube.com/watch?v=ARSoRdHVBX4 "Volume Detection")

### Sample Code
For generating data, we use the built in microphone on Arduino board. We access the microphone data by using the PDM library. In order to update data every timeslot, we write up the code based on Giancono's tutorial about how to get raw sensor data through serial.

bool recordAudioSample() {
    if (mic.hasData() && mic.pop() > SOUND_THRESHOLD) {
        for (int i = 0; i < SAMPLES; i++) {
            while (!mic.hasData())
                delay(1);
            features[i] = mic.pop() * GAIN;
        }

        return true;
    }

    return false;
}
## Part2: Keyword Reconginzer and Print Emoji
---
### Approach Process and Method
1. Recorded 30 seconds dataset for each keyword under both noisy and quiet environment. Similar to part1, we use PDM library to get rms value of voice and store all the value into a csv file. 

2. Used scikit-learn library in Python to train a classifier to distinguish different keywords. 
  Code
3. Use micromlgen library to convert classifier into C code and implement it on Arduino. 
Code
4. We test the keywords accuracy on Arduino, and choose "yes", "no", "happy", "sad" as our keywords. We need to avoid homophones for better result.
Plot ( randomforest, svm, knn) preprocessing data
### Demo:
[![Keyword Detection - Emoji](http://img.youtube.com/vi/aqs0FbGRNAs/0.jpg)](http://www.youtube.com/watch?v=aqs0FbGRNAs "Keyword Detection - Emoji")


## Part3: Keyword Recognizer and Print Characters

[![Keyword Detection - Character](http://img.youtube.com/vi/60HjuuUjA8w/0.jpg)](http://www.youtube.com/watch?v=60HjuuUjA8w "Keyword Detection - Character")

## Strength and Weakness

ML, dataset limited by arduino, connection, looks better.

## Future Direction
1. We can build a GUI app interface to control the LED mask if time allows. For example, users can change patterns, functions or colors they prefer. 

2. We can use Raspberry Pi as our mini-computer, and thus we can implement more function to our LED because it can run multiple programs at same time. With Raspberry Pi we can use voice recognition API from Google Cloud or iFLYTEK, which provides better accuracy and has natural language process helps us determine the emotion of user.

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
## Contribution


## Links

## Reference

https://dalegi.com/2020/06/09/the-hacky-super-loop-arduino-nano-33-ble-sense-example-you-have-been-waiting-for/











## Hardware List / Budget
![budget](images/budget.png)











