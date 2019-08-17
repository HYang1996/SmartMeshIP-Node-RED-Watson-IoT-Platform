Table of Contents
=================
1. [System Structure](#system-structure)
    * [Manager, Mote and Sensors](#manager-mote-and-sensors)
    * [Raspberry Gateway](#raspberry-pi-gateway)
    * [Watson IoT Platform](#watson-iot-platform)
    * [IBM Cloud Node-RED Application](#ibm-cloud-node-red-application)

# System Structure #

The overall structure of the implemented end-to-end system is shown in the digram below:

![](images/structure-diagram.png)

## Manager, Mote and Sensors ##

DC9003A-B SmartMesh IP motes are used in the project. Each mote is connected to various sensors through both digital and analog communication.

Based on the [SmartMesh IP Tools Guide](https://www.analog.com/media/en/technical-documentation/user-guides/smartmesh_ip_tools_guide.pdf) (page 191), there are 4 digital and 4 analog input pins on each mote.

On the sample mote, 2 digital and 2 analog pins are utilised. The humidity and light intensity sensors are analog since their output voltages varies with the environment. On the other hand, the PIR and vibration sensors are digital since their output voltages are either HIGH or LOW.

The DC2274 SmartMesh IP Manager is used in the project, which communicates wirelessly with the motes and receives their health reports, device events and responses.

The manager is connected to the gateway via USB connection, and communicates with the gateway through serial API.

## Raspberry Pi Gateway ##

The gateway to host the manager in this project is the Raspberry Pi due to its small size. Both Raspberry Pi 2 and 3 are tested and verified to be working.

There are two applications running on the gateway. One of them is the JsonServer application that comes with the SmartMeshSDK applications. This application is responsible for the serial API communication between the gateway and the manager. The other application hosted on the gateway is the Node-RED flow. This is an intuitive design to send and receive HTTP requests and responses, and to send MQTT messages to the Watson IoT platform (when the gateway is connected to the internet).

## Watson IoT Platform ##

The Watson IoT Platform is used as a MQTT broker to receive MQTT messages sent and received by both the local and the cloud Node-RED flows.

Various alternatives, such as the Microsoft Azure, Google Cloud IoT Core, and other open source IoT platforms, are also tested. However, the Watson IoT Platform is chosen for the project due to the following advantages:

1. Low cost (free for small projects with an educational account)
1. Flexibility in the format of the JSON messages (other platforms may only support simple telemetry data instead of full JSON strings, largely limiting the applicability of the project)
1. Real-time MQTT messages (other platforms may only support http messages which impose difficulty in real-time communication between the user and the system)
1. Decent integration (the host of the platform, IBM Cloud, is able to host other applications such as the Node-RED flows and databases, allowing easier integration of the system, compared to other multi-platform solutions)

## IBM Cloud Node-RED Application ##

A Node-RED application is created and hosted on the IBM Cloud Service.
