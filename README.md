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

    23/24 - wheel 1/2
    14/15 - wheel 3/4
    8 - mosfet - white
    7 - mosfet - IR
    17 - temperature sensor

<IMG SRC="images/Raspberry-Pi-GPIO-Layout-Model-B-Plus.png" width=200>
       
## To Do

 - Get rid of all reference to sql crap including bobsql. Just save everyhting in a local file.
 
## Change log

 - 20160705 Rebuilding the system for Valerie. I erased the SD card on original Raspbery when installing Trigger Camera on Pi 3 for Zeng You. Copied from robertcudmore.org/raspberry/raspberrycam2/homecage.
 
 
[screen]: https://www.gnu.org/software/screen/
 