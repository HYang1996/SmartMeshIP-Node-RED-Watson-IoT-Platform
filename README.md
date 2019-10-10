Table of Contents
=================
1. [How to Use this Guide](#how-to-use-this-guide)
1. [Getting to Know the Basics](#getting-to-know-the-basics)
    * [SmartMesh IP Network](#smartmesh-ip-network)
        * [Documentations](#documentation)
        * [Online Labs and Recipes](#online-labs-and-recipes)
    * [Node-RED and Watson IoT Platform](#node-red-and-watson-iot-platform)

# How to Use this Guide #

Before using the guide to set up the system, it is worth spending some time to get used to the infrastructure by going through the basic concepts, which are listed in the [next section](#getting-to-know-the-basics).

This guide consists of the following components:

```
1. Basic Setup Guide
2. Gateway
    - Raspberry Pi
3. Watson IoT Platform
4. System Overview
```

The [Basic Setup Guide](Basic-Setup-Guide/README.md) provides a guide with detailed steps to setup the Watson IoT Platform to receive device messages from local Node-RED flows, and it is recommended to be done prior to proceeding to other aspects.

The [Gateway](Gateway/README.md) section showcases how Node-RED flows are implemented for the gateway managers, and how this can be set up on a Raspberry Pi.

The [Watson IoT Platform](Watson-IoT-Platform/README.md) section explains the functionality of the Node-RED flows that are hosted on the Watson IoT Platform, including the online dashboard as well as the SQL database to store the data collected.

Finally, the [System Overview](System-Overview/README.md) section provides an explanation on the overall structure of the project completed, as well as on the software and hardware features of the system.

# Getting to Know the Basics #

Some basic knowledge on each respective aspect of this project is required in order to understand and implement the entire system, and a few useful resources are recommended below:

## SmartMesh IP Network ##

### Documentations ###

1. [SmartMesh IP User's Guide](https://www.analog.com/media/en/technical-documentation/user-guides/SmartMesh_IP_User_s_Guide.pdf)

1. [SmartMesh IP Tools Guide](https://www.analog.com/media/en/technical-documentation/user-guides/smartmesh_ip_tools_guide.pdf)

The documentations on the manager and the mote can be accessed within both the User's Guide as well as the Tools Guide.

### Online Labs and Recipes ###

1. [Dust Academy](https://dustcloud.atlassian.net/wiki/spaces/ALLDOC/pages/40468511/Dust+Academy) (Completing the labs would provide a solid foundation for this project)

1. [dustcloud](https://dustcloud.atlassian.net/wiki/spaces/ALLDOC/overview?mode=global)

## Node-RED and Watson IoT Platform ##

1. [bluemix-experience-workshops](https://github.com/rcruicks/bluemix-experience-workshops/blob/master/Bluemix-Experience-Workshops-V6.md)

1. [smartmesh-bluemix](https://github.com/twatteyne/smartmesh-bluemix)
(This resource also provides many alternatives to this project)

## Node-RED and DashDB ##

1. [Watson IoT Platform - 直接dashDBへデータを格納する](https://qiita.com/egplnt/items/2c911b7618517ebe9ba2)

1. [Node-RED(QuickStart) のデータを dashDB に格納する](http://dotnsf.blog.jp/archives/1047589155.html)

During the course of the project, only Japanese sources with detailed information regarding the integration between Node-RED and DashDB were found. Although the descriptions are in Japanese, the user may wish to infer how the flows could be configured based on the screenshots (both Node-RED flows and JSON strings) provided in the sources.
