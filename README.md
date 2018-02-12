# installBLDCTool
Install the BLDC-Tool on the NVIDIA Jetson TX development Kit. The BLDC-Tool is for use with VESC compatible 4.12 hardware.

These scripts will install the bldc-tool for Vedder Electronic Speed Controller (<b>VESC</b>) and compatible hardware, version 4.12. This type of hardware is sometimes referred to as BLDC controller. The VESC is used in the RACECAR/J project.

The VESC is an open source hardware and software brushless motor controller.

Running the install script builds the bldc-tool, a Qt Gui to interact with the BLDC controller.
Before building the tool, the required prerequisites are installed. 

<em><b>Note:</em</b> The version of libqt5serialport5-dev is 5.5. There is an issue which causes the Bldc-Tool to segment fault when the VESC reboots after being flashed using that version. The work around is to use version 5.6. The scripts builds qtserialport from source and installs it in order to address this issue.</em>

Next the bldc-tool is compiled from source.

Note that this is the tool that can configure and load firmware on the VESC, not the actual firmware that runs on the VESC. The firmware is in a separate repository. See: https://github.com/racecarj/bldc-tool

Compiled versions of the firmware are contained in the bldc-tool repository in the 'firmwares' directory.

The script also downloads VESC configuration files used on the MIT RACECAR. These configurations are located in ~/hardware/vesc

The firmware controls the VESC, the VESC configuration file configures the VESC to interface with the motor being used.



