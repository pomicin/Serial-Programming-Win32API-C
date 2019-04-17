#Serial Port Programming using the Win32 API and the C language.

<img src="http://xanthium.in/sites/default/files/site-images/serial-prog-win32-api/serial-programming-win32-api-tutorial.jpeg">

This repo contains code for transmitting and receiving data serially between an x86 Windows PC and a Microcontroller (the MSP430G2553 microcontroller on the Launchpad development board). The code is written in C and uses the Win32 API calls to control the serial ports on a Windows machine.

<img src="http://xanthium.in/sites/default/files/site-images/serial-prog-win32-api/Serial-port-write-windows.jpeg" alt ="Screenshot of the serial port programming code running on windows 7">
--------------------------------------------------------------------------------------------------------------------------------------
##Details

**Full code explanation along with screenshots can be <a href = http://xanthium.in/Serial-Port-Programming-using-Win32-API> found here on the xanthium website. </a>**

- The Microcontroller and PC are connected in **null modem configuration** using  3 signals (TX, RX, and Ground).

- The code uses standard Win32 API's to initialize the PC serial port and transmit a character to the microcontroller board.
- The PC side code is written in **C** using the **Win32 API**,
- and can be compiled using **MinGW (Minimalist GNU for Windows)** or **Microsoft Visual Studio Express**.

- The code will work with standard **RS232 serial ports** or any **USB to serial converter**.

More info about the  <a href = "http://xanthium.in/USB-to-Serial-RS232-RS485-Converter">USB to Serial/RS232/RS485 converter used in the above tutorial can be found here.</a>

<img src = "http://www.xanthium.in/sites/default/files/site-images/product-page/usb_to_rs485_converter_250px.jpg"  href="http://xanthium.in/USB-to-Serial-RS232-RS485-Converter"/>

- The microcontroller side code is written in **Embedded C** and compiled using **IAR Embedded Workbench for MSP430**.

- The hardware used is the MSP430G2553 Launchpad development board.
 
--------------------------------------------------------------------------------------------------------------------------------------
##Repo Contents 

- **USB2SERIAL_Read**
  - Contains code for **reading data** from the serial port of a Windows machine.
  - A string is transmitted by the **MSP430 Microcontroller** which is received by the PC serial port and then displayed on the console.
  - <img src = "http://xanthium.in/sites/default/files/site-images/serial-prog-win32-api/SerialPort-Read-Received.jpeg"/>
  
- **USB2SERIAL_Write**
  - Contains code for **transmitting data** from the serial port of a Windows machine.
  - A character is **transmitted by the Windows PC** towards the MSP430 Microcontroller.
    The character is received by the MSP430 and an LED on the development board is turned ON to signify data reception. 
  - <img src = "http://xanthium.in/sites/default/files/site-images/serial-prog-win32-api/Serial-port-write-windows.jpeg"/>
