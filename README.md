# ACIT2420_Lab11
## Description
This is a script and service that will generate a weather report using the wttr.in script. It will be saved in a txt file, and is set with a timer to run hourly.

## Installation
1. Download the files
2. Move the script **wthr** to a directory of your choice, or create a default path of **/home/vagrant/week11**.
    1. If you have made a new directory, using your text editor open **wthr.service**
    2. Change the path in ExecStart to match the new path, keeping in mind to keep **/wthr** at the end
    3. The path in WorkingDirectory is where the txt file will be made, you can change this to match the path in ExecStart (without /wthr at the end), or whereever you like
3. Move the service and timer files, **wthr.service** and **wthr.timer**, to **/etc/systemd/system**
4. Reload the daemon list with **sudo systemctl daemon-reload**
5. Enable the timer file (this will also enable your service file) with, **sudo systemctl enable wthr.timer**

## Requirement
**curl** is used in the script. If you do not have it, please install it with **sudo apt install curl**
