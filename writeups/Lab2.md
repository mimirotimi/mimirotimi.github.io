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
    <center><img src="/images/Lab2/mac_add.png" width="450"></center>
</div>
#### Codebase
The Artemis communicates with the computer through a Bluetooth protocol. The MAC address corresponding to the Artemis is queried when trying to connect. Universally Unique Identifiers (UUIDs) helps differentiate the type of data to be sent between the Artemis and computer. UUIDs can be generated using python and must match UUIDs specidied in the Arduino files.
We were provided with demonstration code to verify connection and performance.

## Tasks

#### Task 1
Task 1 requires the computer to send a string to the Artemis and for an augmented message to be returned to the computer. Image 1 below shows the output on the computer, inclusive of the Python code. Image 2 shows the code modified in the Arduino IDE. In order to complete this task, a new command type had to be declared in the Python and Arduino files. 
<div>
 <center>
    <img src="/images/Lab2/Image1.png" width="350">
    <figcaption>Image 1 - Python Code</figcaption>
    <img src="/images/Lab2/Image2.png" width="350">
    <figcaption>Image 2 - Arduino Code</figcaption>
    </center>
</div>

#### Task 2
This task requires the time to be retrieved from the Artemis in milliseconds and be returned in a string format. Image 3 below shows the resulting code in the Python code.
<div>
    <figure>
        <center>
        <img src="/images/Lab2/Task4.png" width="450">
        <figcaption>Image 3 - Python Code</figcaption>
        </center>
    </figure>

</div>

#### Task 3
Task 3 instructs to set up a notification handler to extract the time from the transmitted float value. Because the time on the Artemis was recorded as a float, I decided to transmit it as such. Image 4 shows the result in Jupyter. There was no need to modify code on the Arduino IDE.
<div>
    <figure>
    <center>
    <img src="/images/Lab2/Image4.png" width="450">
    <figcaption>Image 4 - Python Code</figcaption>
    </center>
    </figure>
</div>

#### Task 4
This task requires us to use a notification handler to transmit the temperature of the Arduino in regular 5 second intervals. A challenge that I had with this task was transmitting two different types of data (string & float). Image 5 shows the results from the first challenges I faced, with not all of the data being transmitted. Images 6 and 7 show the Python and Arduino code written, respectively. 
<div>
<center>
    <figure>
    <img src="/images/Lab2/Task5_error.png" width="350">
    <figcaption>Image 5 - Python Code</figcaption>
    <img src="/images/Lab2/Task5.png" width="350">
    <figcaption>Image 6 - Python Code</figcaption>
    <img src ="/images/Lab2/Image7.png">
        <figcaption>Image 7 - Arduino Code</figcaption>
    </figure>
    </center>
</div>

#### Task 5
This tasks requires us to use a notification handler to transmit 50 temperature readings over 100ms intervals. Images 9 and 10 show the Arduino code written, respectively,

#### Task 6
Only around 150 bytes of data can be transmitted from the robot via Bluetooth. Additionally, the Artemis Nano has about 380kB of RAM. This means that a lesser amount can be stored on board, approximately 200kB. The form of "5 seconds of 16-bit values taken at 150Hz" corresponds to an amount of data that exceeds the onboard capabilities. The limitations would result in either non-negligible latency or chunks of data not being transmitted correctly. 

 #### Task 7 (5000-level)
 #### Task 8 (5000-level)
 

