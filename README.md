## Usage

Run each of these in a [screen][screen] session.

    python video.py
    python testhome.py

Detach/exit `screen` sessions but keep the process running with ctrl+a then d

This code uses the class defined in home.py
  
## Features

 - Records video in 5 minute chunks, saving .h264 files into '/home/pi/video/' folder.
 - Turns white light on during the day, 6 AM to 6 PM
 - Turns IR light on during the night, 6 PM to 6 AM
 - Records temperature every 30 seconds (is this correct? Seems too much?)
 - Listens for triggering of 4 magnetic hall sensors (2 per wheel) and records to file. 

All events are logged to file in `/home/pi/video/`. The name of the log file is timestamp for when code is started (YYYYMMDD_HHMMSS.txt).

## Installation

Requires a Raspberry Pi. Clone the repository and run code as described above in 'Usage'.
    
    git clone https://github.com/cudmore/homecageactivity.git
    

## GPIO Pins

|Pin		|Goes To
|:-----		|:-----
|8			|5V Relay channel 1 (white light)
|7			|5V Relay channel 2 (IR light)
|
|17			|DHT22 Temperature/Humidity Sensor
|
|23			|Wheel 1, sensor 1
|24			|Wheel 1, sensor 2
|14			|Wheel 2, sensor 1
|15			|Wheel 2, sensor 2

This image is oriented as if pins on Raspberry Pi are on the top-left.

<IMG SRC="images/Raspberry-Pi-GPIO-Layout-Model-B-Plus.png" width=700>
       
## Parts List

|Item							|Cost		|Link
|:-----							|:-----		|:-----
|Raspberry Pi Model B+/2/3		|	|
|5V >2A AC/DC Adapter
|16GB SD Card (class 10)
|
|Raspberry Pi NoIR Camera (5MP or 8MP)
|Camera Ribbon Cable
|
|SainSmart 5V relay (2 channels)
|IR LEDS
|White LED
|DHT Temperature and Humidity Sensor
|Low Profile Running Wheels (Med Associates)
|4x hall effect sensors
|
|DHT22 Temperature and Humidity Sensor
|
|Wood or 80/20 parts to build frame
|Something to hold camera

## To Do

 - Done: Get rid of all reference to sql crap including bobsql. Just save everyhting in a local file.
 - Write simple plotting and analysis functions
 - Wrap code in web interface (video.py and home.py should be two seperate processes)
 
## Change log

 - 20160705 Rebuilding the system for Valerie. I erased the SD card on original Raspbery when installing Trigger Camera on Pi 3 for Zeng You. Copied from robertcudmore.org/raspberry/raspberrycam2/homecage.
 
 
[screen]: https://www.gnu.org/software/screen/
 