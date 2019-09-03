# Pi-Robot
It is a WiFi controlled video surveillance robot.
Video Surveillance is done using Motion library and robot is controlled through a ssh connection.
## Installation
### First install the motion library:
sudo apt-get install motion
### Set daemon to yes by editing the motion file:
sudo nano /etc/default/motion                                  
start_motion_daemon=yes
### Give permission to save the recorded files:
sudo chown motion:motion /var/lib/motion/
### Edit the motion.conf file :
sudo nano /etc/motion/motion.conf                   
width 640,
height 480,
framerate 60,
stream_quality 90
### Start the video survelliance:
sudo /etc/init.d/motion start                   
You can stop it by: sudo /etc/init.d/motion stop                    
Enter the ip address of the Pi to access the streaming/survelliance.
### Robot:
Change to the directory where pirobot.py file is stored and run it: python pirobot.py
