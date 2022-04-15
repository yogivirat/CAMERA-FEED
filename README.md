# CAMERA-FEED
Video streaming using Raspberry pi zero and Raspberry pi camera Module. 

This project is to deploy the raspberry pi zero W module and raspberry pi camera module to work as video camera and the video can be streamed via computer.

# Before We Start

- Since, the raspberry pi Legacy camera is used in this project, Make sure you have installed RASPBERRY PI OS LITE(LEGACY) on your raspberry pi zero W. For further details, visit https://www.raspberrypi.com/software/.
- Class 10 MicroSD card is recommended for smooth live stream.

# Dependencies 

Install the following dependencies to create camera stream.

```python 
sudo apt-get update 
sudo apt-get upgrade

sudo apt-get install libatlas-base-dev
sudo apt-get install libjasper-dev
sudo apt-get install libqtgui4 
sudo apt-get install libqt4-test
sudo apt-get install libhdf5-dev

sudo pip3 install flask
sudo pip3 install numpy
sudo pip3 install opencv-contrib-python
sudo pip3 install imutils
sudo pip3 install opencv-python

```
