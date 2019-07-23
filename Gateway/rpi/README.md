Table of Contents
=================
1. [Raspberry Pi Setup](#raspberry-pi-setup)
    * [Connect to Eduroam](#connect-to-eduroam)
    * [Update to Jessie](#update-to-jessie)
    * [Install Node-RED](#install-node-red)
1. [Configure Node-RED Flows](#configure-node-red-flows)
    * [Connect to Watson IoT Platform and Device Manager](#connect-to-watson-iot-platform-and-device-manager)

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

If the Pi fails to install Node.js, it can be manually installed before installing Node-RED, and a useful and tested resource can be found [here](https://learn.adafruit.com/node-embedded-development/installing-node-dot-js).

# Configure Node-RED Flows #

The flows used on the Pi are identical to that used on other devices, with some slight modifications in configurations.

The flows can be found in the [rpi-flows.json](rpi-flows.json) file.

## Connect to Watson IoT Platform and Device Manager ##

To connect the flows to the Watson IoT Platform, as well as to configure the Device Manager nodes in the flow, the same procedures introduced in the [Gateway](../README.md) section is used.
