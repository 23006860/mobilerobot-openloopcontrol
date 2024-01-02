# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:
      Take the Ep core robot insert the battery and check the battery percentage 


Step2:
      Turn on the robot and connect the robot to the computer through wifi

Step3:
      open visual studio and import robomaster package and do all the code

Step4:
      Take the measurement of the track on each and every turn and gives the valuse through the code in (m)

Step5:
      run the program to see the robot movement

## Program
```python
from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=0, y=3.05, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=75, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x=1.4, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=0,b=102,effect="on")

    ep_chassis.move(x=0, y=0, z=155, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=225,g=153,b=0,effect="on")

    ep_chassis.move(x=-1.48, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")

    ep_chassis.move(x=0, y=0, z=-45, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=192,b=90,effect="on")

    ep_chassis.move(x=0, y=1.45, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=192,g=137,b=103,effect="on")

    ep_chassis.move(x=2.03, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=85, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=153,b=0,effect="on")

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=204,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=0).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")




    






    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here
![WhatsApp Image 2024-01-02 at 07 41 25_3908df28](https://github.com/23006860/mobilerobot-openloopcontrol/assets/139841752/e1033ad8-84fc-4a8f-b62d-00e47bd02e97
![WhatsApp Image 2024-01-02 at 07 41 26_1db08981](https://github.com/23006860/mobilerobot-openloopcontrol/assets/139841752/cf79602a-fecc-4ac0-96b1-9aba502ca7b7)
![WhatsApp Image 2024-01-02 at 07 41 26_fbd4fe75](https://github.com/23006860/mobilerobot-openloopcontrol/assets/139841752/fcf16e1f-03a8-4785-8a3f-e96b03d8d924)






## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

https://youtu.be/ssExwjamY6A?feature=shared

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
