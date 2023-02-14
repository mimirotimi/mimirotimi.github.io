# Lab 2

<div>
    <p style="float: right; padding-left: 10px;"><img src="/images/Lab2/bluetoothmeme.jpeg" width="450" ></p>
</div>
This lab serves to establish communication between a computer and the Artemis through Bluetooth. For the Python portion a Jupyter lab is used, and the Artemis is programmed through the Arduino IDE. 

### Prelab

#### Setup steps:
1. Installed a virtual environment using 'venv'.
2. Activated the environment using the command 'source FastRobots_ble/bin/activate'.
3. Install the following packages: 'numpy' 'pyyaml' 'colorama' 'nest_asyncio' 'bleak' 'jupyterlab'.
4. Downloaded the codebase found [here](https://cornell.box.com/s/aivj9ad3uv74lmpvxz8s64aamgz6azt1).
5. Started the Jupyter Lab server.
6. Installed ArduinoBLE from the library manager. After burning the code on the Artemis, it published its MAC address. The image below shows the result.
<div>
    <p style="float: center;"><img src="/images/Lab2/mac_add.png" width="450" ></p>
</div>


#### Codebase
The Artemis communicates with the computer through a Bluetooth protocol. The MAC address corresponding to the Artemis is queried when trying to connect. Universally Unique Identifiers (UUIDs) helps differentiate the type of data to be sent between the Artemis and computer. UUIDs can be generated using python and must match UUIDs specidied in the Arduino files.
We were provided with demonstration code to verify connection and performance.


#### Task 1
Task 1 requires the computer to send a string to the Artemis and for an augmented message to be returned to the computer. Image 1 below shows the output on the computer, inclusive of the Python code. Image 2 shows the code modified in the Arduino IDE. In order to complete this task, a new command type had to be declared in the Python and Arduino files. 


#### Task 2
This task requires the time to be retrieved from the Artemis in milliseconds and be returned in a string format. Image 3 below shows the resulting code in the Python code and image 4 shows the code in the Arduino.


#### Task 3
Task 3 instructs to set up a notification handler to extract the time from the transmitted string value. Image 5 shows the result in Jupyter. There was no need to modify code on the Arduino IDE.
 #### Task 4
 #### Task 5
 #### Task 6
 #### Task 7 (5000-level)
 #### Task 8 (5000-level)
 

