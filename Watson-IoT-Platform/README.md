Table of Contents
=================
1. [Introduction](#introduction)
1. [ibmiot Node Configuration](#ibmiot-node-configuration)
1. [Gateway Manual Configuration](#gateway-manual-configuration)
1. [Manager Dashboard](#manager-dashboard)

# Introduction #

Node-RED flows are hosted on the Watson IoT Platform in order to receive messages from the motes and managers, and to enable the user to manipulate and visualise the configurations of the motes and managers anywhere, at anytime.

The detailed setup guide of the Watson IoT Platform Node-RED application can be found in the [Basic-Setup-Guide](../Basic-Setup-Guide/README.md). Once the application is set up, flows ([cloud.json](cloud.json)) can be imported into it.

The file contains 5 individual flows, which are listed below with a short summary of their individual functionality:

1. [__Gateway_Manual_Configuration__](#gateway-manual-configuration): to configure and receive information from a specific manager
1. [__Dashboard_Manager__](#manager-dashboard): to display a dashboard containing information about a specific manager
1. [__Dashboard_Mote__](#dashboard-mote): to display a dashboard containing information about a specific mote connected to a specific manager
1. [__Pin_Status__](#pin-status): to obtain information about the status of each pin on a specific mote
1. [__DB2__](#db2-on-cloud): to store data to the SQL database, DB2 on Cloud

# ibmiot Node Configuration #

The ibmiot nodes are used for the cloud Node-RED flows, which enable the flows to communicate with the Watson IoT Platform:

<img src="images/ibmiot.png" width="200">

Click on any of the node and bring up the following:

<img src="images/ibmiot-configure.png" width="400">

The __Authentication__ method is chosen as __API Key__, and a new API Key can be added:

<img src="images/ibmiot-API.png" width="400">

The __Name__ can be customised, and the next three configurations are done as such:

1. ```API Key : a-f1bk1s-agrwrczy7c```, this is the API Key of the Watson IoT Platform application, which has been created following the [setup guide](../Basic-Setup-Guide/README.md)

1. ```API Token : nEj(AAFOdRT(8CgmH)```, this is the API Token of the Watson IoT Platform application

1. ```Server-Name : f1bk1s.messaging.internetofthings.ibmcloud.com:8883```, this is the server name to connect to. It follows the format as __[orgId].messaging.internetofthings.ibmcloud.com:8883__, where __[orgId]__ is the organisation ID of the Watson IoT Platform applicaiton

Once the API information is configured correctly, the nodes will show as connected when the flow is deployed:

<img src="images/ibmiot-connected.png" width="200">

# Gateway Manual Configuration #

This flow should look like the following:

![](images/gateway.png)

The first part of the flow requires the user to set variables of the flow:

<img src="images/gateway-configure.png" width="400">

Flow variables can be set in the function named "configure here first", and this should be done before the flows are deployed:

<img src="images/gateway-configure-function.png" width="400">

Ther are three variables to be configured:

1. ```flow.set('manager','582857')```, the manager name is the one registered on the Watson IoT Platform (detailed guide under the __Create a Manager Device__ section in the [Basic-Setup-Guide](../Basic-Setup-Guide/README.md)), and the one used here is __582857__

1. ```flow.set('mote',   '00-17-0d-00-00-58-e9-cd')```, the mote name is the full mac address of the mote interested, and the one used here is __00-17-0d-00-00-58-e9-cd__

1. ```flow.set('orgId',  'f1bk1s');```, the organisation ID refers to the one of the Watson IoT Platform application, which can also be found isn the [Basic-Setup-Guide](../Basic-Setup-Guide/README.md), and the one used here is __f1bk1s__

After setting up the variables, the flow can be deployed. When the inject node is pressed, a message should appear to show that the flow variables are configured:

<img src="images/gateway-configure-message.png" width="300">

The second part of the flow enables the user to receive the JsonServerResponse from the manager and messages from the mote:

<img src="images/responses.png" width="400">

The remaining part of the flow allows the user to inject enable/disable of each pin to the mote.

# Manager Dashboard #

This flow allows a manager to be manually configured first, and its information being displayed on the online dashboard:

![](images/dashboard-manager.png)

The node-red-dashboard palette has to be installed first:

<img src="images/node-red-dashboard.png" width="300">

The manager is manully set up in the __configure here first__ function node:

<img src="images/manager-configure.png" width="300">

There are two variables to be configured:

1. ```flow.set('serialPort','/dev/tty.usbserial-00002014D')```, this is the serialPort to which the manager is connected, and the port here is __/dev/tty.usbserial-00002014D__

1. ```flow.set('manager','582857')```, this is the name of the manager that the user wish to connect to, similar to the one configured in the previous flow, and it is __582857__ in this case
