Table of Contents
=================
1. [Introduction](#introduction)
1. [Watson IoT Platform](#watson-iot-platform)
    * [Prerequisite](#prerequisite)
    * [Create Device Types](#create-device-types)
    * [Create a Manager Device](#create-a-manager-device)
    * [Create a Mote Device](#create-a-mote-device)
1. [Node-Red on Local Devices](#node-red-on-local-devices)
    * [Pallets Required](#palletes required)
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

## Create a Manager Device ##

A manager can be created by clicking on the __Create a device__ (will not show up once the first device is created) or the __Add Device__ button, bringing up the page:

![](images/manager-id.png)

The __Device Type__ is selected as __manager___, which has been created as a gateway device type.

There is no fixed format for __Device ID__.

Once reaching the __Security__ step, an __Authentication Token__ is required. This can be left blank for it to be generated automatically:

![](images/manager-token.png)

After finishing all the steps, a new page of the device credentials would be brought up:

![](images/manager-credential.png)

It is __important__ that this page (or the credentials on the page) is saved to be referred to later on since the credentials will not be accessible once leaving this page.

## Create a Mote Device ##

Motes will be automatically created by the manager gateways once the managers establish connections with them. Therefore, a mote device does not have to be created manually here.
