# datameasure
Simulates the problem of reading performance data from devices


## Overview

This is a program to evaluate the capabilits of a person to write software
The applicant shall write a program in either
- Java
- Python

The selection of the language will have an influence on the teams you are eglibe to join

The effort to complete this program should be <4 hours even for a beginner.
There are two optional requirements, which should be completed.

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

sometimes the communication between IP webserver and measurment device fails in this case the value reported might be wrong
sometimes the device reboots and the counter is reset to zero

The result which is interesting for the end user is to get a result curve which is the number of items/10 seconds

## Requirements

- The program should talk with the simulator using a call to http://127.0.0.1/datameasure/data1
- The simulator will answer with data formated as a JSON Object in the form {{"measurepoint": "Point Blanc","data":123}}
- The program should question the simulator every 10 seconds
- data reported from the simulator is the state of a 9bit counter, which might overflow
- the data from the counter shall be converted to a gauge value (which is the difference between two values)
- (optional) If the reported gauge value is changing more then 20% the value shall be skipped
- (optional) if the reported gauge value is changing more then 20% and the counter is less then a gauge value this 
  shall be reported as a reboot and wrong values shall be not reported
  

  

