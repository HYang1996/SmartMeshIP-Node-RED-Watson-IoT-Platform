Table of Contents
=================
1. [Introduction](#introduction)
1. [Gateway](#gateway)
    * [Connect to Watson IoT Paltform](#connect-to-watson-iot-platform)
    * [Connect to Device Manager](#connect-to-device-manager)
1. [Auto-backup](#auto-backup)

# Introduction #

This section details the Node-RED flow used for the gatways (managers) in a SmartMesh IP network. The flow can be implemented on the device where the manager is connected to, such as a laptop or a Raspberry Pi.

The flow is created and improved based on the [resources available](https://github.com/twatteyne/smartmesh-bluemix/tree/master/01-gateway). The following documentation provides detailed explanations to the nodes implemented in the flow.

# Gateway #

## Connect to Watson IoT Platform ##

The first configuration required to be done mannually in the flow is connecting to the device created on the Watson IoT Platform. The nodes that have to be configured are indicated in the screeshot shown below:

![](images/gateway-connect.png)

The proper way to configure these nodes are documented in the [basic setup guide](../Basic-Setup-Guide/README.md), under the __Set up Watson IoT Node__ section.

## Connect to Device Manager ##

Another configuration required to be done mannually is the device manager nodes that are reponsible for deleting the devices on the Watson IoT Platform once they are disconnected from the gateways:

![](images/gateway-device-manager.png)

In order to use the nodes, the [corresponding palette](https://flows.nodered.org/node/node-red-contrib-ibm-wiotp-device-ops) has to be installed:

or install with npm:
```
npm install node-red-contrib-ibm-wiotp-device-ops
```
