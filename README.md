# RESISTIVE TOUCH SCREEN CONTROLLER.


## Table of Contents
1. [Introduction](#introduction)
2. [Bill of Materials/Budget](#bill-of-materialsbudget)
3. [Time Commitment](#time-commitment)
4. [Mechanical Assembly](#mechanical-assembly)
5. [PCB Soldering](#pcb-soldering)
6. [Power up](#power-up)
7. [Unit Testing](#unit-testing)
8. [Production Testing](#production-testing)
9. [Is it Reproducible?](#reproducible)
### Introduction


### Bill of Materials/Budget
![budget](https://user-images.githubusercontent.com/43186158/49831451-ecb8f700-fd61-11e8-9a25-f1d0d24ab567.PNG)
#### So this is the budget that I have made in my fourth week of the Project. As I had'nt buy any thing after that So my budget remained  same till end of the project. If you wanna check the receipts, you can click <a href="https://sahilsaini0014.github.io/ResistiveTouch/#october-2-2018---week-5">here</a>



### Time Commitment
* Time to complete this project would be around 4 days if you have everything handy with the build instruction. It took me couple of weeks to complete this project.In the first week,I had to research about my project, plan my budget accordingly and wait for the items to be delivered. During that time I learned how to connect my Raspberry Pi remotely and researched about my controller more deeply.

* Well, if you are free for couple of days and want to make something interesting, I would suggest you to try this and let me know if you have any questions. My email address is sahilsiani0014@gmail.com. Feel free to contact me.



### Mechanical Assembly
#### Installing OS on Raspberry 
* So After getting each part needed for this project. we can start our project now with installing the Operating Sysytem Noobs on our Raspberry Pi. I have followed the instructions given by the official Raspberry Pi website. Click <a href="https://www.raspberrypi.org/documentation/installation/noobs.md">here</a> to read instructions. To install the OS you also need a monitor, HDMI cable, Keyboard and a mouse. 
If you dont have noobs downloaded, you can download it <a href="https://www.raspberrypi.org/downloads/noobs/">here</a>
* After installing the noobs I have enable the VNC server to connect the Raspberry Pi with my computer remotely which means no wires needed to use the Raspberry Pi. The only thing you need is Power adapter. To Enable and install VNC on your PC you can follow these <a href="https://www.raspberrypi.org/documentation/remote-access/vnc/">instructions</a>  
* So after installing the above things I have connected my controller with my raspberry Pi with jumper wires and tried to see my Controller address(0x41) on Raspberry Pi.
![assembly](https://user-images.githubusercontent.com/43186158/49835163-5f2ed480-fd6c-11e8-82ea-90887ec3f500.JPG)
* I have used the Command: i2cdetect -y 1 
![address](https://user-images.githubusercontent.com/43186158/49835162-5f2ed480-fd6c-11e8-8cdf-eecd440c8d32.JPG)

* Since this Project requires no more than two components, we just have to connect Resistive Touch Screen with the Raspberry Pi connected to the STMPE610 controller. Below are picture while I was making this hardware setup.
![assembling](https://user-images.githubusercontent.com/43186158/49832468-c2b50400-fd64-11e8-9aba-e1f67b316d1f.PNG)

### PCB Soldering
* So to get rid of the above wires that I have showed in the above circuit we can design a PCB. I have used the fritzing app to design my PCB. I have sent my PCB gerber files to Humber prototype lab to get it ready for free of cost.
you can download the files <a href="https://github.com/sahilsaini0014/ResistiveTouch/blob/master/Documents/STMPE610_Gerber.zip">here</a>

* After getting the PCB we have to solder our Controller with the PCB. You should be very careful when soldering the PCB. I have directly soldered the controller on the PCB but you can also use header to raise the height of the controller. Check the pictures below:



### Power Up


### Unit Testing
* And below is my final hardware on which my Resistive Touch Screen is attached on top of the case. Case contains the controller that is soldered with the PCB and that PCB is connected to Raspberry PI.
![finalhardware](https://user-images.githubusercontent.com/43186158/49832625-3a832e80-fd65-11e8-8ddb-e8d743589d05.JPG)


### Production Testing:



### Reproducible?






