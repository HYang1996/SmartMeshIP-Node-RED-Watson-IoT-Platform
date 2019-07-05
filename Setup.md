Table of Contents
=================
1. [Introduction](#introduction)
1. [Watson IoT Platform](#watson-iot-platform)
    * [Prerequisite](#prerequisite)
    * [Create Devices](#create-devices)
    * [Set up a Manager](#set-up-a-manager)
    * [Set up a Mote](#set-up-a-mote)
1. [Node-Red on Local Devices](#node-red-on-local-devices)
1. [Node-Red on Watson IoT Platform](#node-red-on-watson-iot-platform)

# Introduction #

# Watson IoT Platform #

## Prerequisite ##
Firstly, the following apps and services are required to be set up:

![](images/ibm-cloud-apps.png)

Secondly, a connection has to be established between the __*Internet of Things Platform*__ service and the __*Node-RED Starter*__ app as shown below. This can be done in the __*Internet of Things Platform*__ service:

![](images/watson-iot-connections.png)

Note that connecting to the app would involve restaging it. However, it has been noticed that further connections established between other services and the __*Node-RED Starter*__ app would result in the mulfunctioning of the Node-RED flows.

## Create Device Types ##
It is essential that this step is done before proceeding to setting up the managers and motes on the Watson IoT Platform.

After launching the __*Internet of Things Platform*__, device types can be created under the __*Device Types*__ tab:

![](images/create-device-type.png)

By clicking on the __*Add Device Type*__ button, devices can be added.

A manager type can be created by selecting the device __Type__ as __Gateway__:

![](images/create-manager.png)

A mote type can be created by selecting the device __Type__ as __Device__:

![](images/create-mote.png)

After the device types have been created, individual devices can then be created:

![](images/create-device.png)

## Set up a Manager ##

## Set up a Mote ##
