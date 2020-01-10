Table of Contents
=================
1. [Introduction](#introduction)
1. [Design Considerations](#design-considerations)
1. [Circuit Design](#circuit-design)
    1. [Sensors](#sensors)
        1. [PIR Motion Sensor](#pir-motion-sensor)
        1. [Light Intensity Sensor](#light-intensity-sensor)
    1. [Power Supply](#power-supply)
    1. [Power Consumption](#power-consumption)
1. [3D Printed Enclosure](#3d-printed-enclosure)
1. [Deployment Strategy](#deployment-strategy)
1. [Bill of Materials](#bill-of-materials)

# Introduction #

After the establishment of the working communication system from the mote to the gateway and to the Watson IoT Platform, a testbed was designed to utilise the system and showcase its practical feasibility. The objective of the testbed is to take advantage of the input and output ports on the mote to create an indoor environmental data collection device. A gateway (Raspberry Pi with the manager) and multiple motes would be deployed in a room to dynamically monitor the indoor environment simultaneously. The collected data should be accessible online anytime, anywhere, and could be extracted for data analytic purposes.

The following sections would provide a detailed explanation of the hardware designs, and the materials used for the project could be found in the last section, [**Bill of Materials**](#bill-of-materials).

# Design Considerations #

The first design consideration of the testbed is its portability. In order to retrofit a testbed into an existing room, it should be as non-intrusive as possible. Therefore, the testbed should have a relatively small form factor and would not interfere normal functions of, or activities carried out in the room.

As such, the printed circuit board (PCB) which hosts the sensors and circuits would be stacked on top of the mote using the nylon standoffs. The PCB would also have a smaller footprint than the mote, and therefore not increasing the dimension of the footprint. Moreover, the motes would be powered by individual power supplies and therefore not having cable or extensions to the wall, allowing them to be deployed in the room with maximum flexibility.

The second design consideration is the low requirement and ease on repair and maintenance. To reduce frequency of maintenance, particularly the need of recharging the power supply, the power consumption of the system should be as low as possible. This objective led to choices of sensors with extremely low power consumption, and sometimes with a trade-off of its performance.

The last consideration of the testbed is its robustness in deployment. Since the testbeds would be deployed with little supervision and maintenance, they should not be easily susceptible to malfunction and physical damages. In order to achieve this objective, a more finished and solid PCB with soldered components, compared to the prototype breadboard design would be fabricated, and each individual testbed, including the mote, the PCB and the power supply, would be kept in a 3D printed enclosure to protect it from external factors as much as possible.

# Circuit Design #

## Sensors ##

Since the mote could only support analog and digital inputs, digital and analog sensors would be chosen. The digital sensor output should not exceed the supply voltage of the mote at approximately 2.8 V, and the analog sensor output should not exceed 1.7 V when connected to the mote ananlog input pins.

### PIR Motion Sensor ###

The PIR motion sensor is used to detect motion, usually due to human activities, using infrared.

Multiple PIR sensors were tested, and the [adafruit PIR Motion Sensor](https://learn.adafruit.com/pir-passive-infrared-proximity-motion-sensor/overview) was chosen due to its low power consumption as well as the availability of range and delay time adjustment on the sensor.

The sensor has an input voltage range of 5 V - 12 V and outputs a digital signal of 3.3 V.

When deployed, the sensor should face the direction in which human activities are predicted to happen (the sensor itself has a 120 degree detecting angle), and should not face high intensity infrared sources such as sunlight.

### Light Intensity Sensor ###

## Power Supply ##

## Power Consumption ##

# 3D Printed Enclosure #

# Deployment Strategy #

# Bill of Materials #

| Name of Sensor | Price (in GBP) | Supplier with Link |
|:--------------:|:--------------:|:--------:|
|Adafruit PIR Motion Sensor|7.58|[Digi-Key UK](https://www.digikey.co.uk/product-detail/en/adafruit-industries-llc/189/1528-1991-ND/6827035?utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=Google%20Shopping_Sensors%2C%20Transducers&utm_term=&productid=6827035&gclid=EAIaIQobChMI1aLBk6755gIVF-DtCh1vDgU4EAQYASABEgKHLvD_BwE)|
| |9.00|[The Pi Hut](https://thepihut.com/products/adafruit-pir-motion-sensor?variant=27739667793&currency=GBP&gclid=EAIaIQobChMI1aLBk6755gIVF-DtCh1vDgU4EAQYAiABEgKbLvD_BwE)|
|Adafruit Analog Sensor|2.52|[Rapid Electronics](https://www.rapidonline.com/Catalogue/Search?Query=als%20pt19)|
| |2.50|[The Pi Hut](https://thepihut.com/products/adafruit-als-pt19-analog-light-sensor-breakout)|
