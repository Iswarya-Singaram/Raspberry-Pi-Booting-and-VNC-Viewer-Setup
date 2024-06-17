# Raspberry Pi Booting and VNC Viewer Setup
## Project Overview
This project demonstrates how to boot a Raspberry Pi and set it up for remote access using VNC Viewer. The goal is to provide a step-by-step guide to help users get their Raspberry Pi up and running, and enable remote desktop access for convenient management.
<p align="center">
<img src="https://github.com/Iswarya-Singaram/Raspberry_Pi_Booting/assets/145309713/3e69ed7e-2463-44a4-8a45-5048b6319641" width="500" height="300">
</p>

## Prerequisites
Before you begin, ensure you have the following:
<ul>
<li>A Raspberry Pi</li>
<li>SD card</li>
<li>Power supply for the Raspberry Pi</li>
<li>Ethernet cable or Wi-Fi dongle</li>
<li>Monitor and HDMI cable (optional)</li>
<li>Keyboard and mouse (optional)</li>
<li>Another computer or Laptop for VNC Viewer</li>
</ul>

<p align="center">
<img src="https://github.com/Iswarya-Singaram/Raspberry_Pi_Booting/assets/145309713/0ebee90f-4034-4570-bf42-e66d7ed007bd" width="500" height="300">
</p>

Note: Setting up VNC on a Raspberry Pi involves using both a desktop and a laptop for the initial configuration. Initially, a desktop is required to enable VNC on the Raspberry Pi. Once VNC is enabled, the laptop can be used to connect to the Raspberry Pi via VNC. After this initial setup, the laptop alone can be used for further viewing and interaction with the Raspberry Pi. While it is possible to perform the initial setup directly using a laptop, my project specifically employs both a desktop and a laptop for the initial configuration.

## Software Installation
### Initial Boot:
1. Download and install the Raspberry Pi Imager and the latest raspberry pi OS from the official Raspberry Pi website.
   ~~~
   https://www.raspberrypi.com/software/
   ~~~
2. Insert the SD card into your computer using an SD card reader.
3. Open the Raspberry Pi Imager, select the Version of Raspberry Pi you have, Raspberry Pi OS, and the storage where it needs to be written.
   
   <p align="center">
<img src="https://github.com/Iswarya-Singaram/Raspberry_Pi_Booting/assets/145309713/65134045-9312-46c6-9088-946c8367bbc3">
</p>

4. Click on the additional settings and enable SSH (for VNC viewer) and set up the SSD and password(so that raspberry pi can connect wirelessly to the mentioned SSD), then click on Next.

 <p align="center">
<img src="https://github.com/Iswarya-Singaram/Raspberry_Pi_Booting/assets/145309713/5ebf8f99-d7c1-4e4f-bca9-53266434026c">
</p>


5. Once the imaging process is complete, remove the SD card from your computer and insert it into the Raspberry Pi.
6. Connect the Raspberry Pi to a monitor using an HDMI cable.
7. Connect the keyboard and mouse to the Raspberry Pi.
8. Connect the Ethernet cable or set up the Wi-Fi.
9. Power up the Raspberry Pi by connecting the power supply.
10. Complete the initial setup process, including setting up the locale, time zone, and Wi-Fi

## Enable VNC Server in Pi
1. Open the terminal on the Raspberry Pi.
2. Update the package list and upgrade all packages:
~~~
sudo apt update
sudo apt upgrade
~~~
3. Install the RealVNC server
~~~
sudo apt install realvnc-vnc-server
~~~
4. To enable VNC from the Raspberry Pi Configuration tool:
<li>Open the Raspberry Pi Configuration tool from the Preferences menu.</li>
<li>Go to the "Interfaces" tab.</li>
<li>Enable VNC.</li>
  
<p align="center">
<img src="https://github.com/Iswarya-Singaram/Raspberry_Pi_Booting/assets/145309713/c7026b02-60d4-4a80-a00e-c809633426ac" width="500" height="300">
</p>

## VNC Viewer Setup
1. Download and install VNC Viewer on your computer from the RealVNC website.
~~~
https://www.realvnc.com/en/connect/download/vnc/?lai_sr=5-9&lai_sl=l
~~~
2. Open VNC Viewer and sign in or create an account if needed.
3. Click on the "+" icon to add a new connection.
4. Enter the IP address of your Raspberry Pi and give it a name.
5. Click "OK" to save the connection.
6. Double-click on the new connection icon to start the session.
7. When prompted, enter the username and password for your Raspberry Pi (default is "pi" and "raspberry" unless changed).

<p align="center">
<img src="https://github.com/Iswarya-Singaram/Raspberry_Pi_Booting/assets/145309713/4169f94a-8a42-4eac-a7a8-01fe3713f7e7" width="500" height="300">
</p>

## Troubleshooting
### Cannot Connect to Raspberry Pi
<li>Ensure the Raspberry Pi is powered on and connected to the network.</li>
<li>Check the IP address and ensure it is correct.</li>
<li>Ensure VNC Server is running on the Raspberry Pi.</li>

### VNC Server Not Running
<li>Make sure you have enabled the VNC server in the Raspberry Pi Configuration tool.</li>
<li>Check the status of the VNC server by running:</li>

~~~
sudo systemctl status vncserver-x11-serviced.service
~~~
## Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue to discuss your ideas.
   


