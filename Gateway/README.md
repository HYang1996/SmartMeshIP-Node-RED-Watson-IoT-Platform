Table of Contents
=================
1. [Introduction](#introduction)
1. [Gateway](#gateway)
    * [Connect to Watson IoT Paltform](#connect-to-watson-iot-platform)
1. [Auto-backup](#auto-backup)

# Introduction #

This section details the Node-RED flow used for the gatways (managers) in a SmartMesh IP network. The flow can be implemented on the device where the manager is connected to, such as a laptop or a Raspberry Pi.

The flow is created and improved based on the [resources available](https://github.com/twatteyne/smartmesh-bluemix/tree/master/01-gateway). The following documentation provides detailed explanations to the nodes implemented in the flow.

# Gateway #

## Connect to Watson IoT Platform ##

The first configuration required to be done mannually in the flow is connecting to the device created on the Watson IoT Platform. The nodes that have to be configured are indicated in the screeshot shown below:

![](images/gatewat-connect.png)

The proper way to configure these nodes are documented in the [basic setup guide](../basic-setup-guide/README.md), under the __Set up Watson IoT Node__ section.
