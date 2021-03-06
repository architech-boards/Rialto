.. _quick:

Quick start guide
*****************

Hardware requirements
---------------------

- Silica Rialto Board kit 
- One or more USB type-A extension cable 
- PC with terminal software (such as HyperTerminal)

.. image:: _jn_photo/wise_usb.jpg

Software requirements
---------------------

- Jennic SDK toolchain (JN-SW-4041), JN5168 stack library (JN-SW-4065) and Flash GUI tool (JN-SW-4007)
- Rialto_Jennic firmware 
- PC terminal emulator (such as HyperTerminal)

.. note::

 | **If you have not yet installed Eclipse Jennic, before proceeding, go to:**
 | :ref:`Jennic Suite Install`

Hardware setup
--------------

Plug Rialto Board into USB port (also using USB type-A extension cable)

.. image:: _jn_photo/usb_plug.jpg

with USB type-A extension cable

.. image:: _jn_photo/usb_cable.jpg

Wait for properly USB dongle driver installation

.. image:: _jn_images/ftdi230.jpg

When drivers are ready you can connect one or more Rialto Board (at least two for firmware evaluation)

.. image:: _jn_images/ftdi230_ready.jpg

.. tip::

 | **See Control Panel of your PC and note COM Port number configured for each Rialto Board (figure above).**
 | For any troubles during USB driver installation in Windows XP see at :ref:`ftdixp`

.. image:: _jn_images/usb_port.jpg

*Connecting two Rialto Board (minimun number for full firmware evaluation), take care at COM number installed on your PC*

.. image:: _jn_images/2usb.jpg

.. _seriz:

SerizII plugin
==============
Rialto board has in bottom layer two strip (6 and 4 way) and can be used as a plugin for SerizII. 

.. image:: _jn_photo/seriz_wise.jpg

.. important::

 Before using Rialto boards as SerizII plugin, you must download and install the proper firmware revision of the SerizII board (**SerizRialto.zip**). For all instruction and information about, see at `Silica SerizII <http://www.silica.com/seriz2>`_ 


**Take care plugging Rialto on SerizII: be shure that both boards (Rialto and SerizII) are power off before!!**

.. _hyper:

HyperTerminal settings
----------------------

Set your HyperTerminal COMx parameter:

| speed = 115200 baud
| data with =  8
| parity = none
| stop bit = 1
| flow control = none

.. image:: _jn_images/com_set.jpg 

In Ascci Setup windows, check "Send line ends with line feeds"


.. image:: _jn_images/com_crlf.jpg 


Rialto Board FW installation & setup
-------------------------------------

- In the folder C:\\Jennic\\Application create new folder named **Rialto_Jennic** 

.. image:: _jn_images/wise_work_folder.jpg 

- Unzip all files from Rialto_Jennic_1_0.zip into the folder **C:\\Jennic\\Application\\Rialto_Jennic** just created 

.. image:: _jn_images/folder.jpg 

- Go to Start --> Jennic --> JN-SW-404x products --> Eclipse and click on to start Jennic Eclipse

.. image:: _jn_images/start_1.jpg

- Check if workspace setting is like figure below. Then click OK to proceed.

.. image:: _jn_images/start_2.jpg

- Now you can see the Eclipse Main Window

.. image:: _jn_images/screen_1.jpg

- Select menu File --> Import

.. image:: _jn_images/import_1.jpg

- In the dialog box that will open, click on **General**, select **Existing Projects Into Workspace** and after click "Next" button: new dialog will open.

.. image:: _jn_images/prj_import.jpg

- Click on "Browse..." button an navigate to **C:\\Jennic\\Application\\Rialto_Jennic** folder. Click on "OK" button

.. image:: _jn_images/prj_import_2.jpg

- Check options and setting as the image below, then click "Finish" button to import project.

.. image:: _jn_images/prj_import_3.jpg

- Wait for project import, then you can see Rialto_Jennic project in the Project Explorer windows of Eclipse Platform.

.. image:: _jn_images/project_ready.jpg

- **First of all**, right click over "Rialto_Jennic" in the Project Exporer window, then select "Clean Project". After cleaning, a first build will start automaticaly

.. image:: _jn_images/import_5.jpg

- Take care at image above. Expand project, and see at "Console" tab: you can find a log that ends with "Generating binary .... Rialto_Coord_JN5168.bin"

.. image:: _jn_images/clean&build.jpg

.. tip:: **If you can't see in the "Console" tab the message above, make shure that "Build Automatically" option (inside "Project" menu) is set**

 .. image:: _jn_images/aut_build.jpg

.. note:: **The binary file for Coordinator has been generated and ready for Rialto Board programming**

.. tip:: *don't care if you have this warning (see Problems tab).* 

 .. image:: _jn_images/warning.jpg

- Now you can build End_Node project. Click on drop-down arrow next to Hammer Icon (blue circled in image below)

.. image:: _jn_images/build_1.jpg

then click on "Rialto_EndD". Build will start.

.. image:: _jn_images/build_2.jpg

- When build has finished, in the Project Explorer tab expand Rialto_Coord and Rialto_EndD Build folders. The result in image below.

.. image:: _jn_images/compile.jpg

**You have built the two binary files and you are ready for program Rialto Board**

Programming Rialto Board with Flash GUI Tool
---------------------------------------------

**Before starting Flash GUI programmer tool, you must connect Rialto Board whit built-in USB dongle. Please refer to Hardware Setup chapter on this document to check connection**

- Flash Gui Tool can be accessed by clicking on the drop-down arrow next to Tools Symbols on the toolbar, then selecting **"Flash GUI Tool"**

.. image:: _jn_images/tools_1.jpg

*Dont't care of error in Console tab: no troubles or malfunctioning will be affect board program!*

.. image:: _jn_images/error_flash_gui.jpg

- See at Flash GUI windows: check if version is **1.8.9**. If not, refer :ref:`progup` on **Installing Jennic Developement Suite** guide

.. image:: _jn_images/flash_1.jpg

| - **Step 1**: make these actions:
| 1) Check and/or select appropriate COM port (green circled). 
|    You can find find out which serial communications port your PC has allocated to the Rialto Board by checking in the Control Panel-->Hardware-->device Manager-->COM port
| 2) Click on "Refresh" button (blue arrow) and check the result (orange circled): if device not appear, check cable and USB connection (COM port installed)
| 3) Select in the Baud rate drop-down menu "500000" (for maximun programming time performace)
| 4) Check "Automatic Program and Reset" checkbox (brown arrow)

.. image:: _jn_images/flash_2.jpg

.. note:: **Take care at COM port: if it's already busy with other applications (such as HyperTerminal), you cannot find it in COM port dropdown menu of Flash GUI Tool**

- **Step 2**: click "Browse" button red circled, navigate to **C:\\Jennic\\Application\\Rialto_Jennic\\Rialto_Coord\\Build** and select bin file **"Rialto_Coord_JN5168.bin"**. Then click "Open" button.

.. image:: _jn_images/flash_3.jpg

| - **Step 3**: in the "Program" window will appear **C:\\Jennic\\Application\\Rialto_Jennic\\Rialto_Coord\\Build\\Rialto_Coord_JN5168.bin**. 
|	Clik on "Program" button to start board programming.

.. image:: _jn_images/flash_4.jpg

- **Step 4**: wait for verifyng...

.. image:: _jn_images/flash_5.jpg

- **Step 5**: Click "OK" button and board will reset and start.

.. image:: _jn_images/flash_6.jpg

.. tip:: **To program End-Node, repeat from step 2 but navigate to C:\\Jennic\\Application\\Rialto_Jennic\\Rialto_EndD\\Build and select "Rialto_EndD_JN5168.bin"**
 **When you have programmed even Coordinator that End-node, you can select FW binary by clicking the drop-down arrow (red circled in image below) and select from drop-down menu** 

 .. image:: _jn_images/flash_set.jpg

| Now you have finished all setup necessary to evaluate, debug and make changes inside Rialto Firmware.
| You can plug the Rialto boards into USB ports of your PC, open HyperTerminal sessions and use Serial Monitor command for evaluate the main Firmware functions.
| For further details you can read the guides:

:ref:`monitor`

:ref:`tips`
