MobileRobot-Openloopcontrol
Aim:
To develop a python control code to move the mobilerobot along the predefined path.

Equipments Required:
RoboMaster EP core
Python 3.7
Procedure
Step1:

Use from robomaster import robot

Step2:

Choose the x,y,z - axis movement distance(meters).

Step3:

Give ep_chassis.move to move straight.

Step4:

Give time.sleep() for a break.

Step5:

Give ep_chassis.drive_speed to have a circular movement.

Program:
Developed by: vedagiri indu sree Register No: 23004520

from robomaster import robot
import time
from robomaster import camera
```
if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.64, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")

    ep_chassis.move(x=0.4, y=0, z=80, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=-1.5, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=63, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")

    ep_chassis.move(x=1.6, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=225,effect="on")

    ep_chassis.move(x=0, y=0, z=40, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")

    ep_chassis.move(x=1.35, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=90, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on") 

    ep_chassis.move(x=2, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=80, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=51,effect="on")    

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=0,effect="on")    

    ep_chassis.move(x=0, y=0, z=0, xy_speed=0).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=0,effect="on")   

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```    

    


MobileRobot Movement Image:

![WhatsApp Image 2023-12-26 at 16 15 22_c6006412](https://github.com/vedagiriindusree/mobilerobot-openloopcontrol/assets/149366776/70dc8e66-a10d-4cc3-9fef-fdea6b0fc261)

![image](https://github.com/vedagiriindusree/mobilerobot-openloopcontrol/assets/149366776/96536f6c-85c6-4e15-aed1-ed1de558ce36)

MobileRobot Movement Video:
https://youtu.be/p4HoSFZrcbQ?si=J8HucPYXssL-1JnK



Result:
Thus the python program code is developed to move the mobilerobot in the predefined path. Developed by: vedagiri indu sree Registration No: 23004520


Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
About
No description, website, or topics provided.
Resources
 Readme
License
 BSD-3-Clause license
 Activity
Stars
 0 stars
Watchers
 0 watching
Forks
 443 forks
Report repository
Releases
No releases published
Packages
No packages published
Languages
Python
100.0%
Footer
