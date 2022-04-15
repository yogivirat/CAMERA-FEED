# VIDEO-STREAM
Video streaming using Raspberry pi zero and Raspberry pi camera Module. 

Arthur  :  https://github.com/yogivirat

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
# Steps to follow.

- Open up terminal and clone the Camera Stream repo:
  ```
  cd /home/pi
  git clone https://github.com/yogivirat/CAMERA-FEED.git
  ```
- Launch Web Stream
  
  Note: Creating an Autostart of the main.py script is recommended to keep the stream running on bootup.
  ```
  sudo python3 /home/pi/CAMERA-FEED-main/main.py
  ```

- Autostart your Pi Stream
  
  A good idea is to make the the camera stream auto start at bootup of your pi. You will now not need to re-run the script every time you want to create the stream.     You can do this by going editing the /etc/profile to:
  
  ```
  sudo nano /etc/profile
  ```
  Go the end of the and add the following (from above):
  
  ```
  sudo python3 /home/pi/CAMERA-FEED-main/main.py
  ```
  This would cause the following terminal command to auto-start each time the Raspberry Pi boots up. This in effect creates a headless setup - which would be accessed   via SSH. Note: make sure SSH is enabled.
  
- View in any devices.
  
  In this step, make sure your raspberry pi zero W and your computer are connected to same Wifi. Go to your Web browser(Google Chrome, Edge etc.), and type the IP
  address of your Raspberry pi zero W and add :5000 For example, if your raspberry pi zero W IP address is 192.168.43.84, then type the following in your web browser :
  
  ```
  192.168.43.84:5000
  ```
  Now you can able to view the video stream in your devices such as PC, Mobiles etc. 
  
 # Work with OpenCV.
 
  Since the raspberry pi zero W has 512 MB RAM, it is very slow in running OpenCV on its own. You can use this live stream video as a video input to your OpenCV project. For this, make sure your raspberry pi zero W and the computer in which you are working with OpenCV project are connected to same WiFi. 
  
  In your OpenCV project, create the Video Capture object using the following command :
  
  ```
    # define a video capture object
    vid = cv2.VideoCapture("http://your-raspberryPI-IP-Address/video_feed") 
  ```
    
  For example, if IP address of your raspberry pi zero W is 192.168.43.84, then type the following command :
  
  ```
   # define a video capture object
   cap=cv2.VideoCapture("http://192.168.43.84:5000/video_feed")
  ```
 
 
This Project is very useful in many ways such as surveillance camera and in Camera in Prometric Examination Halls.

Happy Coding !!
