Table of Contents
=================
1. [Raspberry Pi Setup](#raspberry-pi-setup)
    * [Connect to Eduroam](#connect-to-eduroam)
    * [Update to Jessie](#update-to-jessie)
    * [Install Node-RED](#install-node-red)

# Raspberry Pi Setup #

In this project, the Raspberry Pi 2 is used to host the SmartMesh Network manager.

## Connect to Eduroam ##

Firstly, the Raspberry Pi has to be connected to the eduroam network via Wifi.

The script and instructions used to do so can be found under the folder [eduroam-config](eduroam-config).

## Update to Jessie ##

In order to install Node-RED preperly, the Pi has to be updated from Wheezy to Jessie.

A useful and tested tutorial to do so can be found in this [link](https://www.howtoforge.com/tutorial/how-to-upgrade-debian-wheezy-to-jessie-stable-release/).

## Install Node-RED ##

Once the system is set up, Nore-RED can be installed with the code:

```
bash <(curl -sL https://raw.githubusercontent.com/node-red/raspbian-deb-package/master/resources/update-nodejs-and-nodered)
```

If the Pi fails to install Node.js, it can be manually installed before installing Node-RED, and a useful and tested resource can be found [here](https://learn.adafruit.com/node-embedded-development/installing-node-dot-js)
