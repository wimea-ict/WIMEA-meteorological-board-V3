
I2C meteorological break-out board V3
=====================================

News i V3
---------
* Third generation/revision of project daughterboard
* Using one channel ADC MCP3421 for more compact design
* Side-by-side BME280 for evaluation. Uses I2C address 0x76
* T/RH chips at edge of chip for better air-flow 
* Thermal barrier for T/RH to minimize heating from other components.
* MS5611 for Pressure is removed and replaced by BME280 on sensornode.

Introduction
------------
This I2C board uses selected sensors by the WIMEA project. WIMEA-ICT 
Research Component 3 has focus on Automated Weather Station  (AWS) 
development and network densification in Africa. The work is funded 
by Norad. 

The idea is challenge existing technologies in price performance aspect
by using the latest research and products and combining expertise in
various fields.

The work herein describes a break-out board with selected sensors to be
used as an first approximation for prototyping, verification and testing.
The results are open and can be used in various project as well as being 
a starting point for other. The work includes:

* Sensor selection and testing
* PCB design
* Some comparison

The sensor selection
--------------------

* SHT25 (Sensiron)  Temp, RH and via calculation AH, temp dew-point, heat index.
http://www.sensirion.com/fileadmin/user_upload/customers/sensirion/Dokumente/Humidity/Sensirion_Humidity_SHT25_Datasheet_V3.pdf

* Optional. BOSH BME280. T/RH/P
https://ae-bst.resource.bosch.com/media/_tech/media/datasheets/BST-BMP280-DS001-19.pdf

* MCP3421 (1 channel. Hi-Res 18-bit ΔΣ ADC with Differential Input)
http://ww1.microchip.com/downloads/en/DeviceDoc/22003b.pdf

The selected sensors are proposed by Joachim Reuder, Björn Pehrson, Robert 
Olsson and WIMEA team. Thanks to Andrew Seidl for evaluation of the BME280 
pressure sensor.

The PCB
--------
The break-out board was designed with the gEDA PCB toolchain. Major components
gschem and pcb. I2C bus is available on many platforms, Arduino, Raspberry Pi and is available on most microcontrollers. Included:

* gEDA schematics and resource files
* gerber files for fabrication
* various pictures

Schematics
-----------
![Component side] (./pictures/dboard-3-schematics.png)

References & Project Site
--------------------------
http://gfi063214.klientdrift.uib.no
