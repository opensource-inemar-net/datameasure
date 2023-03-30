# datameasure
Simulates the problem of reading performance data from devices


## Overview

This is a program to evaluate the capabilits of a person to write software
The applicant shall write a program in either
- Java
- Python

The selection of the language will have an influence on the teams you are eglibe to join

The effort to complete this program should be <4 hours even for a beginner.

After finishing the task please zip your result and send it to the human resource responsible person.
Please don't fork the repository.

If you have any question regarding the requirements make a sensible assumption and document this assumption.

It is a simulation of retrieving measument data from an embedded device. 

## Background

Within the repositiory you find:
 - this file with the description of requirements for the program
 - a simulator that simulates the embedded device (java -jar dataembedded.jar)
 - the source code of the simulator
 

The simulator simulates an embedded measurment device.
The device consists on an IP webserver and a subcomponent that does the actual measurment. 
The actual measurement device is connected via a not so stable connection to the IP webserver.

The measurement device is counting items on a conveyor belt using a 9 bit counter.
The speed of the conveyor belt is changing over time.

The result which is interesting for the end user is to get a result curve which is the number of items/10 seconds


