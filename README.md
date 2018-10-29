# HeatBoard
This project started on a personal requirement which is to control the Heater at home via a web application or an android application. I started using the items I already have so it will be a custom project but might be usefull for anyone interested.

Basic Requirements :
--------------------
1) The heater is Vaillant brand combi without remote control panel in downstairs
2) We should be build a device to mechanically control vaillant's heat control knobe
3) We should read the environment temperature back for
   a) not to burn up the house
   b) to have a feedback to control the temperature if needed
   c) be sure the hause is heated enough 
4) The device must have wifi connection capability
5) Device should run a web page for easy control
6) Web page must have authentication control
7) DC 5V or a battery should be sufficient to power the device
8) The device should have a blinking heartbeat LED
9) TBD

Basic Design :
--------------

Equipment decisions :
- Microcontroller with Wifi support will be a "NodeMCU"
- Mechanical controller hardware will be a servo
- The temperature sensor will be "TBD"

Software Interfaces :
- "/" page should ask for login if not authenticated
- Authentication tokens should be carried out to every request\
- The interface should display the current temperature
- There should be a setting for target temperature
- There should be shortcut buttons for different target temperatures
- The selection will be applied when the user presses "APPLY" button
- The commands will be handled by different URLs to be used as web services for direct requests
   e.g. /targetTempSet   /readCurrentTemp
   
 ![Basic Design](https://github.com/barisdinc/HeatBoard/blob/master/Docs/HomeDuino.png)
 
 TODO : 
 ------
 - Finish the NodeMCU implementation
 - Finish Webb application
 - Try developing an Android App
 - Temperature controller should be a seperate ESP-01 on and stair
 - OTA support will be added
 
