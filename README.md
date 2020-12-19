# ECE_M202A_MASK --- TEAM CL

This Project is for ECE M202A at UCLA

## Team Member:
Hongyi Chen

Rui Lin

## Overview
---
### Motivation
Under the tough COVID-19 pandemic, thousands of people lost their lives and lots of hospitals' ICUs are hitting capacity. However, there are a lot of people still not wearing masks. The team members aim to design a special PPE to encourage more people to wear the mask which helps stop the spread of virus. A mask doesn’t have to hide the smiling while protecting people from possible COVID-19 infection. Thus, the Voice-Activated LED facial mask we built is not only a PPE, but also a wearable IoT device which implements BLE and various sensors. It can protect users from viruses while mimicking their talking or smiling even when their mouth is hidden behind the protective cloth. 


### Goals
Design and build a mask which can detect the voice volume, detect the keyword, recognize the sound of crying and smiling under a noisy environment by machine learning, and output different patterns on LED.  

### Hardware List
1. Arduino Nano 33 BLE Sense

2. 8*8 Flex LED Panel

3. 1200 mAH Lithium Battery

4. Battery Charger

5. Facial Mask (desire black)

## Prior Work
<a target="_blank" rel="noopener noreferrer" href="https://docs.edgeimpulse.com/docs/audio-classification" >Edge Impulse Audio Classification</a>

The Online Edge Impulse provides an easier way to apply machine learning and train the model, but it is hard to collect the dataset online due to the delay. Our team decides to develop an arduino program to collect data and implement the Micromlgen to train the model. 

## Implementation
Our team use the built-in microphone on Arduino Nano 33 BLE Sense board as the input device  and connect a 8*8 Flexible LED Panel to GPIO Pin 6 as the output. For the power supply, our team decides to use the 1200 mAH Lithium Battery to power both the board and the LED display. 
![Pinout](images/Pinout.png =250x)
The structure of the facial mask is three layers, like a sandwich. The Arduino board, LED Panel and the Battery are fixed by tape on the inner side of the outer mask. The black color’s mask is preferred in order to obtain better light output. The inner mask is replaceable for healthy concern since CDC advises to change facial mask every four hours.  The pictures below are the prototype of the facial mask.

![circuit](images/circuit.jpg)


## System Architecture
---
![flowchart](images/pipeline.png)


Our project is mainly divided into three parts. The following content will introduce the functions and technical approach in each part.
## Part 1: Volume Amplitude Detection and Output  
---
### Function:
The LED panel embedded in the facial mask can display different angles of the mouth-opening pattern by detecting voice volume. The arduino program can extract the peak of RMS value from sound for a certain period, and we set a certain threshold for loud and silent situations. 
 
###Process
Implement the PDM library to extract the RMS value from the built-in microphone.
Design different bitmaps for different patterns.
Use a case structure to display and optimize by setting delay.
### Demo:
[![Volume Detection](http://img.youtube.com/vi/ARSoRdHVBX4/0.jpg)](http://www.youtube.com/watch?v=ARSoRdHVBX4 "Volume Detection")

### Sample Code
For generating data, we use the built-in microphone on an Arduino board. We access the microphone data by using the PDM library. In order to update data every time slot, we write up the code based on Giancono's tutorial about how to get raw sensor data through serial.
![read_data](images/read_data.PNG)

## Part2: Keyword Recognizer and Print Emoji
---
### Approach Process and Method
1. Recorded 30 samples for each keyword under both noisy and quiet environments as the dataset. And, stored all the values into a csv file for each keyword.

Code

2. Developed a python program by using scikit-learn library to train a classifier which can distinguish certain keywords. 
3. Used Micromlgen library to convert classifier into C code and deploy on Arduino board. 

Code

4. Tested the accuracy of detecting keywords on Arduino, and chose "yes", "no", "happy", "sad" as our keywords. (Need to avoid homophones for better results)

Plot ( randomforest, svm, knn) preprocessing data

### Demo:
[![Keyword Detection - Emoji](http://img.youtube.com/vi/aqs0FbGRNAs/0.jpg)](http://www.youtube.com/watch?v=aqs0FbGRNAs "Keyword Detection - Emoji")


## Part3: Keyword Recognizer and Print Characters

Demo for printing keywords on LED display by detecting certain keywords.
[![Keyword Detection - Character](http://img.youtube.com/vi/60HjuuUjA8w/0.jpg)](http://www.youtube.com/watch?v=60HjuuUjA8w "Keyword Detection - Character")

## Strength and Weakness

Strength:
1.

Weakness:
1.

ML, dataset limited by arduino, connection, looks better.

## Future Direction
1. Built a GUI app interface to control the LED mask if time allows. For example, users can change patterns, functions or colors they prefer. 

2. Use tjeRaspberry Pi as our mini-computer, and thus we can implement more function to our LED because it can run multiple programs at same time. With Raspberry Pi we can use voice recognition API from Google Cloud or iFLYTEK, which provides better accuracy and has natural language processing techniques that helps us determine the emotion of the user.

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












