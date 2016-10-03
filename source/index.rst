.. Rialto Board by Silica Architech  documentation master file, created by
   sphinx-quickstart on Thu Jul 25 11:13:41 2013.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Rialto Board by Silica Architech's documentation!
===============================================================

:Version: 1.00
:Copyright: (C)2016 Avnet Silica company
:Date: 30 july 2013

.. image:: _jn_images/nxplogo.gif
.. image:: _jn_images/jennic.gif

.. index:: index

**INTRODUCTION**
****************

| Silica Rialto Board is useful system to evaluate a basic IEE802.15.4 network using JN5168 wireless module. 
| Rialto board has a single built-in USB dongle. Simply switching serial channel from terminal application to programming software, you can perform two alternate functions:
| a - Evaluate network with simple serial monitor (using a PC terminal such as HyperTerminal)
| b - Program Firmware into JN5168 module (using JN-SW-4007-Flash-Programmer v1.8.9)

*If you want, you can use separate USB-TTL adapter connected with 6 pin strip on Rialto board. In this case, you can have two separate serial channel, first (USBdongle) for programming and second (6 pin strip) for Serial Monitor. See* :ref:`serial`

Rialto board is also designed as a plugin for SerizII board. **Rialto "ready to run" kit** is specially designed for quick use and fast evaluate  network functionallity. All you have to do is plug End-Node on SerizII board, plug Coordinator on PC USB port, start HyperTerminal and enjoy!!

With Rialto board you can evaluate the performance of new NXP SENS300/01 device. The SEN300/01 integrates one high-accuracy temperature sensor, four relative humidity
sensors, six light sensors, a user-writable non-volatile memory and a 10-bit
analog-to-digital converter. Rialto application reads out basic data from temperature, humidity and light sensors. For more information about this sensor, see at NXP official site `NXP official site <http://www.nxp.com/>`_ 

Rialto board integrates a NTAG203F, NFC Forum Type 2 Tag compliant IC with 144 bytes user
memory and field detection. This device is used on SerizII labs. See at official documentation page of NXP site `NTAG203F <http://www.nxp.com/search?q=ntag203f&type=typenumber&rows=10>`_ 

| Firmware application was developed with JN-SW-4041-SDK-Toolchain-v.1.1 (Eclipse based). 
| You must also install JN-SW-4065-JN516x-JenNet-IP-SDK-v857 software library. 
| Firmware project is included in Rialto_Jennic.zip file.
| Reference guide are included into Install.zip and are:
|   1) JN-UG-3064 - Software Developer’s Kit Installation and User Guide
|   2) JN-UG-3007 - JN51xx Flash Programmer User Guide

Install.zip also include JN-SW-4041-SDK-Toolchain-v.1.1.exe and JN-SW-4065-JN516x-JenNet-IP-SDK-v857.exe to install developement suite.

| For JN5168 modules programming, you must install FlashGUI programmer from JN-SW-4007 (included in Install.zip). Please, note that JN-UG-3007 refers to Flash GUI programmer version 1.8.4, and JN-SW-4047 contains new release 1.8.9 of Flash GUI programmer. See release note document included in JN-SW-4047 package. The release 1.8.9 must be installed for JN516x modules programming.
| Install.zip and Rialto_Jennic.zip files can be downloaded from Rialto section of Silica ArchiTech web page (registration needed)
| **Installing Jennic Developement Suite** chapter will guide you through the basic steps of the installation procedure of Jennic Developement Suite

We suggest you to read first the Quick Start Guide to perform a correct Firmware setup. 

:ref:`quick`

This guide explains how to use this application and provides an overview of on the structure of the project firmware

.. toctree::
 :maxdepth: 3
   
 JenInst
 quick
 ready
 PrjFiles
 Monitor
 tip

 
 

 
 
We also suggest you to see documentation `JN516x Wireless Microcontrollers <http://www.nxp.com/techzones/wireless-connectivity/jn51xx/jn516x.html>`_ for any specific further detail.

* :ref:`search`

