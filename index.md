# CENG 317 - RESISTIVE TOUCH CONTROLLER.

## November 19, 2018 - Week 12
#### Last week PCB power up was due but, I was unsuccessful to do that. I was getting an error. So This week I tried again to get it work. Then I read the code again and got the mistake that I did. As in last class you told me that my code can run with both I2C or SPI. My conntroller is connected to the Raspberry Pi through I2C only but, I was trying to run it with SPI simpletest code that I took from Github. So I just changed That from SPI to I2C and finally I got the Results. Now my Controller is working properly. I know that I got my results late but I have learnt alot by this mistake. As you can see my results below:
#### When I run my file output result ask the user to touch
![stmpe610_1](https://user-images.githubusercontent.com/43186158/48745511-a6c4b380-ec39-11e8-92eb-827c1b68638c.PNG)
#### When the user touch the Resistive Touch Screen connected to the controller then he can get the postion and pressure readings. Position is displayed X and Y cordinates. As You can see the picture attached below that first reading is X cordinate on the Touch Screen and Second one is Y cordinate and Third One is Pressure applied while touching the Screen. 
![stmpe610_2](https://user-images.githubusercontent.com/43186158/48745507-a4faf000-ec39-11e8-8ae9-4fb81dcb079c.PNG)





## November 13, 2018 - Week 11
#### So this is the week 11 of this course. PCB power up was due this week. As you that I have tried very hard to make it work but unfortunately, I was not able to achieve my goal on the same day. As I had tried to run each and every code that I had found on github related to my controller (<a href=https://www.adafruit.com/product/1571> ResistiveTouch Screen Controller</a>). Libraries and test code for my controller is also given by <a href= https://github.com/adafruit/Adafruit_STMPE610 >adafruit</a> But these libraries is for arduino and I am not using the arduino for my project. So I had found the CircuitPython code from the github licensed by MIT. But to run this code I had to install <a href =https://learn.adafruit.com/circuitpython-on-raspberrypi-linux/overview>CircuitPython</a> on Raspberry Pi. Then I had installed CircuitPython on my Rasberry Pi. But I got some chip version error in that code. I had also told uh the problem that I was going through. Then you suggested me to try some other code of CircuitPython to run on my RaspberryPi. Then I had tried to blink the LED by the <a href =https://learn.adafruit.com/circuitpython-on-raspberrypi-linux/digital-i-o>Code</a> available on the adafruit website. Finally I got successful in blinking the LED with that code. I also showed to you the blinking of LED. This means that CircuitPython is properly working on my RaspberryPi. Now I will try to solve the error that I am getting in my code.

### Blinking the LED.
![img-0794](https://user-images.githubusercontent.com/43186158/48524820-dc3f5a80-e84f-11e8-89dc-98a47631b0bb.JPG)


## November 6, 2018 - Week 10
## PCB Soldering
### Soldered PCB Connecetd with the RPI
#### As You can see my <a href= https://www.adafruit.com/product/1571>sensor</a> Soldered with the PCB and that PCB Connected to my Raspberry Pi With the header. I was lucky in this case that I got my PCB working in the very first case. I was able to see my controller address on the Raspberry Pi terminal by running the command "sudo i2c detect -y 1"   My overall hardware is too compact. So this is a benefit for me. I can easily put everything in a small case.
![img-0578](https://user-images.githubusercontent.com/43186158/48318126-ca4c8600-e5c9-11e8-92fc-5fbfacfaeaf4.JPG)

### Soldering the Resistive Touch Screen Controller with the PCB
#### This the Week 10 and I got my designed PCB from the prototype lab. So I have soldered my STMPE610 Controller with my PCB Board. This was a good experience for me. As I did it for the first time but it was looking very good. Better then I expected. 
![img-0576](https://user-images.githubusercontent.com/43186158/48318128-cb7db300-e5c9-11e8-9e1c-7223c88c4b8e.JPG)

## October 30, 2018 - Week 9

## PCB Design
#### So this is week 9 and I have done half of my project.This week we have to design a PCB to connect our sensor with the Raspberry PI so we can carry our hardware easily. With the PCB we can get rid of all the wires and the breadboard. So I have designed my PCB board on Fritzing app and sent the gerber files to the Humber prototype lab to get the PCB Board ready in few weeks.
![stmpe610_pcb](https://user-images.githubusercontent.com/43186158/47757858-be35ff80-dc7e-11e8-971b-710924b082fc.png)


## October 23, 2018 - Week 8

## Fritzing Diagram
![stmpe610_bb](https://user-images.githubusercontent.com/43186158/47757856-bd04d280-dc7e-11e8-86da-812758063072.jpg)

## Schematic Diagram
![stmpe610_schem](https://user-images.githubusercontent.com/43186158/47757860-bf672c80-dc7e-11e8-8a80-aa23efbef1d0.png)


## Connection Created
As you can see my Controller I2C Address on RPI terminal. 
I also successfully able to use my RPI on my laptop by using VNC viewer.
![img-0126](https://user-images.githubusercontent.com/43186158/47398153-d64ad380-d700-11e8-8c98-a2ee172ccc4e.JPG)

## Raspberry Pi connection With the Controller
![img-0125](https://user-images.githubusercontent.com/43186158/47398149-d3e87980-d700-11e8-90d3-3f8838fec31f.JPG)
## Soldered Controller 
![img-0123](https://user-images.githubusercontent.com/43186158/47398147-d21eb600-d700-11e8-813b-93167bb0b021.JPG)


## October 16, 2018 - Week 7
## Pseudo Assignment(UML Diagram)

![uml](https://user-images.githubusercontent.com/43186158/47397533-b49c1d00-d6fd-11e8-860a-e3356aa21fe8.PNG)

## Started Soldering the Controller

![img-0120](https://user-images.githubusercontent.com/43186158/47397369-efea1c00-d6fc-11e8-82ef-dd5009e6c5e1.JPG)


## October 2, 2018 - Week 5
## Proof of Purchases

### CanaKit Raspberry Pi 3 b+

![raspberry](https://user-images.githubusercontent.com/43186158/46378852-ee33b800-c66a-11e8-8b2a-75a6e47cf173.PNG)
#### So Me and my friends ordered 6 Raspberry Pies together. So this is the invoice for all of Us. It cost me like $73 for a Raspberry Pi

### Controller and Resistive Touch Screen

![sensor](https://user-images.githubusercontent.com/43186158/46379249-32738800-c66c-11e8-862a-4b7ee04807ab.PNG)
#### So i ordered my Controller with my friend. Highlighted products are mine on the invoice above 

### Jumper Wires and SD card
![wires](https://user-images.githubusercontent.com/43186158/46379834-1c66c700-c66e-11e8-893d-94a2c6aa2b4c.PNG)

## September 25, 2018 - Week 4
## Budget
#### So below are my all expenses for everything I need in my project
![budg](https://user-images.githubusercontent.com/43186158/47396571-5ec57600-d6f9-11e8-88ff-884b811b659c.PNG)

#### Son this gantt chart explains all the planning for my project.
## September 18, 2018 - Week 3
## Schedule

![schedule](https://user-images.githubusercontent.com/43186158/47396869-9a147480-d6fa-11e8-9632-ec4b828bfb44.PNG)

## September 11, 2018 - Week 2
## Proposal
#### So with the proposal I proposed my idea and my project. 
![proposal](https://user-images.githubusercontent.com/43186158/47396387-7819f280-d6f8-11e8-97ac-5888ca0b90c9.PNG)

## September 04, 2018 - Week 1
## Blinking the LED
In the very first week i have tried to blink the LED with Raspberry pi.
I have also decided my Controller.

