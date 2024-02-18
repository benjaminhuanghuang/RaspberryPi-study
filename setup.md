From Raspberry Pi and Arduino, Install Raspberry Pi OS Without a Monitor (Recap)

## Install Raspberry Pi OS without monitor

1. Download Raspberry Pi Imager from https://www.raspberrypi.org/software/

2. Connect the SD card to your computer.

3. Open Raspberry Pi Imager. Choose the OS "Raspberry Pi OS(32-bit)" and the SD card.

4. Click "Settings" and enable "SSH", "WiFi", set username and password, set locale settings.

5. Click "Write" to write the OS to the SD card.

## Find the IP address of Raspberry Pi
Angry IP Scanner: https://angryip.org/download/
Add "MAC Vendor" to the columns.
Find IP of "Raspberry Pi Trading"

## SSH to Raspberry Pi

Delete the known_hosts file in .ssh folder if you have trouble connecting to the Raspberry Pi.

```bash
    ssh pi@<ipaddress>
```

## Enable the VNC in Raspberry Pi

SSH to the Raspberry Pi and run the following command to enable VNC.
```bash
    sudo raspi-config 
    > 3 Interface Options > I3 VNC > Yes

    > 1 System Options > S5 Boot / Auto Login > B4 Desktop Autologin

    > 2 Display Options > D5 VNC Resolution > 1920 x 1080

    sudo reboot
```

## Connect to Raspberry Pi using VNC

Download realvnc VNC Viewer from https://www.realvnc.com/en/connect/download/viewer/


## Install Arduino IDE on Raspberry Pi

The Arduino provided by apt-get is not the latest version.
Download "Arduino IDE" ARM32 bit online

```bash 
    wget https://downloads.arduino.cc/arduino-1.8.16-linuxarm.tar.xz
    tar -xvf arduino-1.8.16-linuxarm.tar.xz
    sudo mv arduino-1.8.16 /opt
    cd /opt/arduino-1.8.16
    sudo ./install.sh
```

## Config file
