Table of Contents
=================
1. [Introduction](#introduction)
1. [Gateway_Manual_Configuration](#gateway-manual-configuration)

# Introduction #

Node-RED flows are hosted on the Watson IoT Platform in order to receive messages from the motes and managers, and to enable the user to manipulate and visualise the configurations of the motes and managers anywhere, at anytime.

The detailed setup guide of the Watson IoT Platform Node-RED application can be found in the [Basic-Setup-Guide](../Basic-Setup-Guide/README.md). Once the application is set up, flows ([cloud.json](cloud.json)) can be imported into it.

The file contains 5 individual flows, which are listed below with a short summary of their individual functionality:

1. [__Gateway_Manual_Configuration__](#gateway-manual-configuration): to configure and receive information from a specific manager
1. [__Dashboard_Manager__](#dashboard-manager): to display a dashboard containing information about a specific manager
1. [__Dashboard_Mote__](#dashboard-mote): to display a dashboard containing information about a specific mote connected to a specific manager
1. [__Pin_Status__](#pin-status): to obtain information about the status of each pin on a specific mote
1. [__DB2__](#db2-on-cloud): to store data to the SQL database, DB2 on Cloud

# Gateway_Manual_Configuration #

This flow should look like the following:

![](images/gateway.png)

The first part of the flow requires the user to set variables of the flow:

![](images/gateway-configure.png)

Flow variables can be set in the function named "configure here first", and this should be done before the flows are deployed:

![](images/gateway-configure-function.png)

Ther are three variables to be configured:

1. ```flow.set('manager','582857')```, the manager name is the one registered on the Watson IoT Platform (detailed guide under the __Create a Manager Device__ section in the [Basic-Setup-Guide](../Basic-Setup-Guide/README.md)), and the one used here is __582857__
1. 
