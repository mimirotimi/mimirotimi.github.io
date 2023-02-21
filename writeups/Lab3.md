# Lab 3 - TOF Sensor

### The purpose of this lab is to equip the robot with sensors - the faster the robot can sample and the more it can trust a sensor reading, the faster it is able to drive.

## Pre-Lab

The Time-of-Flight sensor used is based on the VL53L1X. When using two sensors, I will use the approach of switching on and off of both sensors while accessing their respective shutdown pins. I will likely place the sensors at the front and on the side of the robot; this will lead to a major blindspot on the opposite side but I am working on thinking of some work around solutions and the encorporation of additional sensors. Likely,the robot will miss obstacles on the opposing side or even on the reverse when/after performing stunts.
In this lab, we will setup a Time-of-Flight (ToF) sensor, which is based on the VL53L1X. Please skim the manual, and check out the datasheet before beginning this lab. Note the sensor I2C address.
When cutting wires, I kept them relatively long to allow future adaptability. The circuit diagram is shyown below in Figure 1.

While you can choose to ignore the robot in this lab, you will have to permanently cut wires, and so it is worth doing so with their position in the robot in mind, such that you won’t have to redo too much later on. Discuss your thinking in the write-up. Sketch out a diagram of all the wires you will need to connect:

## Lab

Figure 2 below shows a picture of my final soldered setup, inclusive of the Artemis baord. The shorter cable was used to attach the breakout board to the Artemis. 

#### Task 1

The example wireI2C code returns the I2C address as 0x29. The datasheet specifies the TOF address as 0x52 so this was a bit surprising. However, the TOF sensor has a read/write bit, resulting in the address being displayed as 0x29 due to the shifted bit. 


The sensor has 3 modes: short, medium and long (which is the default). I think that the long detection mode will be ideal for detection up ahead, especially as the robot moves forward. On the side, the medium mode may work better, especially for mapping purposes as well. I think that the short detection mode may not be the most applicable, especially if the robot does not need to manoeuver tight corners and turns. 

#### Task 2

I have decided to use the long distance sensing mode, since it will likely be used on the front of the robot. Below, Figure 3 shows the reading as shown in the Arduino serial monitor/plotter. Figure 4 shows a plot of the sensed values at a range of distances in between 1mm and 10000mm in intervals of 100mm; it was plotted using matplotlib. 

#### Task 3
