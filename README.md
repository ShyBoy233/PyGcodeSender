# pyGcodeSender
A simple python script to send gcode file using serial to various machines.

# 1. A brief introduction
This is a simple python script to send gcode file using serial to various machines, such as 3D printer, laser engraving machine, CNC machine and etc.
The script has currently been tested on Windows 10 to send a gcode file to a DIY 3D printer (MKS TinyBee motherboard and Marlin firmware). The gcode file was generated using UtiMaker Cura.

Features
>- Automatically detects available serial port
>- Update sending status dynamically
>- Programmatically sends gcode over a USB port
>- Easy to use, only needs pyserial and tqdm installed python3 environment

# 2. Usage
## Help function
```console
C:\Users\Administrator\Desktop>python pyGcodeSender.py --help
usage: pyGcodeSender [-h] [-p port name] [-b baud rate] filename

A simple python script to send gcode file using serial to various machines.

positional arguments:
  filename              gcode to be sent

options:
  -h, --help            show this help message and exit
  -p port name, --port port name
                        serial port
  -b baud rate, --baudrate baud rate
                        baud rate, default 115200
```
## A demo usage
```console
C:\Users\Administrator\Desktop>python pyGcodeSender.py cude.gcode
====================================================================================================
Welcome to use this simple python script to send gcode file using serial.

Current setting:
        Filename: cude.gcode
        Port name: COM4
        Baud rate: 115200

Would you like to continue with these settings?[y/n]y

Codes in file cude.gcode have been loaded successfully.

Trying to connect to port COM4.
Port COM4 has been successfully connected.

Sending codes.
100%|██████████| 8726/8726 [27:05<00:00,  5.37 codes/s, gcode=;SETTING_3 l = 80\\nsupport_wall_count

All codes have been sent successfully.
Congratulation!!!

Welcome to use this simple script again. Best wishes.
====================================================================================================
```

# 3. Notes
1. <mark>Caution:</mark> **When you use this script for the first time in a new environment, please always monitor the running status of your machine to avoid unexpected situations.**
2. Basic idea taken from https://github.com/grbl/grbl