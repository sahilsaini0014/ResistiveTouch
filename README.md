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
So Resistive Touch Screen Controler is used to control a  Resistive Touch Screen of any size. This breakout board features the STMPE610, which has both I2C and SPI interfaces available. There is also an interrupt pin that you can use to indicate when a touch has been detected to your microcontroller or microcomputer. We wrapped up the chip with a 3V voltage regulator and level shifting so it's safe to use with 3V or 5V logic. Its a nicely designed chip, and has very stable precise readings.


![intro](https://user-images.githubusercontent.com/43186158/49844583-919ef880-fd91-11e8-9941-a645798a0393.PNG)




### Bill of Materials/Budget
#### Required parts to make this harware:
##### <a href="https://www.canakit.com/raspberry-pi-3-model-b-plus-basic-kit.html">Raspberry Pi 3 Model B+ Basic Kit</a> 
##### <a href="https://www.adafruit.com/product/1571">Resistive Touch Screen Controller - STMPE610</a>
##### <a href="https://www.adafruit.com/product/333">Resistive Touch screen - 3.7" Diagonal</a>
##### <a href="https://www.amazon.ca/Haobase-120pcs-Multicolored-Female-Breadboard/dp/B01DLKLL6C/ref=s">Jumper Wires</a>
##### <a href="https://www.amazon.ca/Sandisk-Ultra-Micro-UHS-I-Adapter/dp/B073K14CVB/ref=sr_1_4?s=electronics&ie=UTF8&qid=1537837988&sr=1-4&keywords=micro%2Bsd%2Bcard%2B16gb&th=1">Sd card 16Gb</a>
![budget](https://user-images.githubusercontent.com/43186158/49831451-ecb8f700-fd61-11e8-9a25-f1d0d24ab567.PNG)
* So this is the budget that I have made in my fourth week of the Project. As I had'nt buy any thing after that So my budget remained  same till end of the project. If you wanna check the receipts, you can click <a href="https://sahilsaini0014.github.io/ResistiveTouch/#october-2-2018---week-5">here</a>



### Time Commitment
* Time to complete this project would be around 4 days if you have everything handy with the build instruction. It took me almost 11 Weeks to complete this project. In the first five weeks,I had to research about my project, plan my budget accordingly and wait for the items to be delivered. During that time I learned how to connect my Raspberry Pi remotely and researched about my controller more deeply.

* Well, if you are free for couple of days and want to make something interesting, I would suggest you to try this and let me know if you have any questions. My email address is sahilsiani0014@gmail.com. Feel free to contact me.



### Mechanical Assembly
#### Installing OS on Raspberry 
* So After getting each part needed for this project. we can start our project now with installing the Operating Sysytem Noobs on our Raspberry Pi. I have followed the instructions given by the official Raspberry Pi website. Click <a href="https://www.raspberrypi.org/documentation/installation/noobs.md">here</a> to read instructions. To install the OS you also need a monitor, HDMI cable, Keyboard and a mouse. 
If you dont have noobs downloaded, you can download it <a href="https://www.raspberrypi.org/downloads/noobs/">here</a>
* After installing the noobs I have enable the VNC server to connect the Raspberry Pi with my computer remotely which means no wires needed to use the Raspberry Pi. The only thing you need is Power adapter. To Enable and install VNC on your PC you can follow these <a href="https://www.raspberrypi.org/documentation/remote-access/vnc/">instructions</a>  
* So after installing the above things I have connected my controller with my raspberry Pi with jumper wires and tried to see my Controller address(0x41) on Raspberry Pi.
![assembly](https://user-images.githubusercontent.com/43186158/49835163-5f2ed480-fd6c-11e8-82ea-90887ec3f500.JPG)
* I have used the Command: sudo i2cdetect -y 1 
![address](https://user-images.githubusercontent.com/43186158/49835162-5f2ed480-fd6c-11e8-8cdf-eecd440c8d32.JPG)

### PCB Soldering
* So to get rid of the above wires that I have showed in the above circuit we can design a PCB. I have used the fritzing app to design my PCB. I have sent my PCB gerber files to Humber prototype lab to get it ready for free of cost.
you can download the files <a href="https://github.com/sahilsaini0014/ResistiveTouch/blob/master/Documents/STMPE610_Gerber.zip">here</a>

##### PCB design
![design](https://user-images.githubusercontent.com/43186158/49842415-762fef80-fd89-11e8-969c-bba81af9c7a1.png)
* After getting the PCB we have to solder our Controller with the PCB. You should be very careful when soldering the PCB. I have directly soldered the controller on the PCB but you can also use header to raise the height of the controller. Check the pictures below:
##### While Soldering the PCB with controller
![soldering](https://user-images.githubusercontent.com/43186158/49840905-6f05e300-fd83-11e8-9266-eb07374173dd.JPG)
##### Mounted Controller on the Raspberry Pi through PCB
![donesoldering](https://user-images.githubusercontent.com/43186158/49840906-6f05e300-fd83-11e8-92e0-0ff43badfa76.JPG)


### Power Up
* So by making the PCB we have made our hardware safe and compact. Now this the time to power up the hardware and get the touch readings by touching the Sreen. So the very first step you should take to power up the hardware is to install the CircuitPython on our Rasberry Pi. Because I had used the python code in my project to get the readings.
* To install the CircuitPython on your Raspberry PI follow these Instructions <a href="https://learn.adafruit.com/circuitpython-on-raspberrypi-linux/installing-circuitpython-on-raspberry-pi">here</a>
* After installing the CircuitPython on your Raspberry Pi you should try to blink an LED with the code given in the instructon. I had checked the it by blinking an LED.
![led](https://user-images.githubusercontent.com/43186158/49841691-8abeb880-fd86-11e8-9b68-1c1960b14e88.JPG)
* If you are able to blink the LED then you are ready to run the actual code. First try the command: Sudo i2cdetect -i 1 to double check your controller address. Because if your PCB have some connection problem than you will not be able to see your controller address on raspberry Pi.
* So copy all the files from my repository to your Raspberry pi. Click here to see the files. I have got this code from github and it was licensed by MIT. But the test file that I have got from github was for SPI connections. But we are using the I2C connection for our project. So I have code the test file for I2C connection by myself.
* The only thing you have to do is simply run the Simpletest.py file with the command: python3 simpletest.py and then You will get Screen like this:
![run](https://user-images.githubusercontent.com/43186158/49842341-1e918400-fd89-11e8-9f89-edc7361ce896.PNG)
* When you will touch the Screen you will get the following readings:
![readings](https://user-images.githubusercontent.com/43186158/49842340-1df8ed80-fd89-11e8-9555-74c47515d40a.PNG)


### Unit Testing
* So until this point softwere part is almost done. Now we should make a case for our hardware to keep it more safe otherwise you can break your screen easily.
* In my Case I have sent the case design <a href="https://github.com/sahilsaini0014/ResistiveTouch/blob/master/Documents/STMPE610.cdr">corel draw file</a> to Humber prototype lab and got the unassemblled Case next day.
##### Case Design:
![casedesign](https://user-images.githubusercontent.com/43186158/49842748-c065a080-fd8a-11e8-97ff-225f7b59eecc.JPG)
##### Un-assembled Case:
![unassembled](https://user-images.githubusercontent.com/43186158/49842749-c065a080-fd8a-11e8-949d-2d246f813ad8.JPG)

* And below is my final hardware on which my Resistive Touch Screen is attached on top of the case. Case contains the controller that is soldered with the PCB and that PCB is connected to Raspberry PI.
![finalhardware](https://user-images.githubusercontent.com/43186158/49832625-3a832e80-fd65-11e8-8ddb-e8d743589d05.JPG)

### Production Testing:
* If we want this product to produce on large scale and then the testing this hardware can be fully automated by machines. Because As you know this is an Resistive Touch Screen Controller that basically works when the pressure is applied on the screen. So no human hand is needed. So Testing can be done by the Machines. Soldering part can be easily done by the machines on very fast pace.

### Reproducible?
* As from top to bottom of this page I have elaborated each and every step clearly and in very easy way. So to reproduce the same hardware should not be much difficult now. You just have to focus on the instructions I gave and and the instructions in the links that I have provided. You should not miss any step while installing anything.






