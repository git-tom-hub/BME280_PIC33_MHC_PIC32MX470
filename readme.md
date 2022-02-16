---
grand_parent: Reference Applications
parent: Curiosity PIC32MX470 Development Board
title: Getting Started
nav_order: 1
---
<img src = "images/microchip_logo.png">
<img src = "images/microchip_mplab_harmony_logo_small.png">

# Getting Started Application on Curiosity PIC32MX470 Development Board
<h2 align="center"> <a href="https://github.com/Microchip-MPLAB-Harmony/reference_apps/releases/latest/download/pic32mx470_getting_started.zip" > Download </a> </h2>

-----
## Description

>  The application reads the current room temperature from the temperature sensor on the MikroElectronika Weather click board.
	The temperature read is displayed on a serial console periodically every 500 milliseconds. The periodicity of the temperature
	values displayed on the serial console is changed to one second, two seconds, four seconds, and back to 500 milliseconds every
	time you press the switch S1 on the Curiosity PIC32MX470 Development Board. Also, LED1 is toggled every time the temperature is
	displayed on the serial console.

## Modules/Technology Used:

- Peripheral Modules      
	- I2C   - No, I changed to SPI. Couldn't get the i2C to work "out of the box"
	- Timer
	- Core Timer
	- GPIO
	- UART
	- DMA

## Hardware Used:

- [Curiosity PIC32MX470 Development Board](http://www.microchip.com/DevelopmentTools/ProductDetails.aspx?PartNO=DM320103)   
- [MikroElectronika Weather click board](https://www.mikroe.com/weather-click)
- [MikroElectronika USB UART click board ](https://www.mikroe.com/usb-uart-click)


## Software/Tools Used:
<span style="color:blue"> This project has been verified to work with the following versions of software tools:</span>  

Refer [Project Manifest](./firmware/src/config/pic32mx470_curiosity/harmony-manifest-success.yml) present in harmony-manifest-success.yml under the project folder *firmware/src/config/pic32mx470_curiosity*  
- Refer the [Release Notes](../../../release_notes.md#development-tools) to know the **MPLAB X IDE** and **MHC/MCC** Plugin version.  
- Any Serial Terminal application like Tera Term terminal application.

<span style="color:blue"> Because Microchip regularly update tools, occasionally issue(s) could be discovered while using the newer versions of the tools. If the project doesn’t seem to work and version incompatibility is suspected, It is recommended to double-check and use the same versions that the project was tested with. </span> To download original version of MPLAB Harmony v3 packages, refer to document [How to Use the MPLAB Harmony v3 Project Manifest Feature](https://microchip.com/DS90003305)

## Setup:  
- Connect the Type-A male to mini-B USB cable to mini-B DEBUG USB port to power and debug the PIC32MX470 Curiosity Development Board.
- Connect the MikroElectronika Weather click board on the mikroBUS interface 1
- Connect the MikroElectronika USB UART click board on the mikroBUS interface 2
- Connect USB Type-A male to mini-B male cable to USB-UART serial port through mikroBUS interface 2  
<img src = "images/hardware_setup.jpg" width="500" height="325" align="middle">

## Programming hex file:
The pre-built hex file can be programmed by following the below steps

### Steps to program the hex file
- Open MPLAB X IDE
- Close all existing projects in IDE, if any project is opened.
- Go to File -> Import -> Hex/ELF File
- In the "Import Image File" window, Step 1 - Create Prebuilt Project, click the "Browse" button to select the prebuilt hex file.
- Select Device has "PIC32MX470F512H"
- Ensure the proper tool is selected under "Hardware Tool"
- Click on "Next" button
- In the "Import Image File" window, Step 2 - Select Project Name and Folder, select appropriate project name and folder
- Click on "Finish" button
- In MPLAB X IDE, click on "Make and Program Device" Button. The device gets programmed in sometime.
- Follow the steps in "Running the Demo" section below

## Programming/Debugging Application Project:
- Open the project (pic32mx470_getting_started\firmware\pic32mx470_curiosity.X) in MPLAB X IDE
- Ensure "Starter Kits (PKOB)" is selected as hardware tool to program/debug the application
- Build the code and program the device by clicking on the "Make and Program Device" button in MPLAB X IDE tool bar
- Follow the steps in "Running the Demo" section below

## Running the Demo:
- Open the Tera Term terminal application on your PC (from the Windows® Start menu by pressing the Start button)
- Change the baud rate to 115200
- You should see the temperature values (in °F) being displayed on the terminal every 500 milliseconds, as shown below  

  <img src = "images/result1.png" width="425" height="235" align="middle">  
- Also, notice LED1 blinking at a 500 millisecond rate  
- You may vary the temperature by placing your finger on the temperature sensor (for a few seconds)  
  <img src = "images/temp_sensor_placement.jpg" width="500" height="325" align="middle">  
- Press the S1 switch on the Curiosity PIC32MX470 Development Board to change the default sampling rate to one second  
  <img src = "images/user_button_placement.jpg" width="500" height="325" align="middle">  
  <img src = "images/result2.png" width="345" height="165" align="middle">  
- Every subsequent press of switch S1 on the Curiosity PIC32MX470 Development Board changes the default sampling rate to two seconds, four seconds, 500 milliseconds and back to one second in cyclic order as shown below  
  <img src = "images/result3.png" width="315" height="440" align="middle">  
- While the temperature sampling rate changes on every switch S1 press, notice LED1 toggling at the same sampling rate

## Comments:
- Reference Training Module: [Getting Started With Harmony v3 Peripheral Libraries on PIC32MX 470 MCUs](https://microchipdeveloper.com/harmony3:pic32mx470-getting-started-training-module)
- This application demo builds and works out of box by following the instructions above in "Running the Demo" section. If you need to enhance/customize this application demo, you need to use the MPLAB Harmony v3 Software framework. Refer links below to setup and build your applications using MPLAB Harmony.
	- [How to Setup MPLAB Harmony v3 Software Development Framework](https://www.microchip.com/mymicrochip/filehandler.aspx?ddocname=en1000821)
	- [How to Build an Application by Adding a New PLIB, Driver, or Middleware to an Existing MPLAB Harmony v3 Project](http://ww1.microchip.com/downloads/en/DeviceDoc/How_to_Build_Application_Adding_PLIB_%20Driver_or_Middleware%20_to_MPLAB_Harmony_v3Project_DS90003253A.pdf)  

## Revision:
- v1.4.0 - Added MCC support, regenerated and tested application.
- v1.3.0 - Regenerated and tested application.
- v1.2.0 - Regenerated and tested application.
- v1.1.0 - Regenerated and tested application.
- v1.0.0 - Released demo application
