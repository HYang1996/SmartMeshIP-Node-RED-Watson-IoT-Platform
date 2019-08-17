Table of Contents
=================
1. [System Structure](#system-structure)
    * [Manager, Mote and Sensors](#manager,-mote-and-sensors)

# System Structure #

The overall structure of the implemented end-to-end system is shown in the digram below:

![](images/structure-diagram.png)

## Manager, Mote and Sensors ##

DC9003A-B SmartMesh IP motes are used in the project. Each mote is connected to various sensors through both digital and analog communication.

Based on the [SmartMesh IP Tools Guide](https://www.analog.com/media/en/technical-documentation/user-guides/smartmesh_ip_tools_guide.pdf), there are 4 digital and 4 analog input pins on each mote.

On the sample mote, 2 digital and 2 analog pins are utilised. The humidity and light intensity sensors are analog since their output voltages varies with the environment. On the other hand, the PIR and vibration sensors are digital since their output voltages are either HIGH or LOW.
