---
layout: post
title: SuRF Development Kit
---

SuRF is the kit developed by Texas Instruments mainly used in carrying out research in Wireless Sensor Networks.

**Installing MSPGCC with Eclipse**

Go to the below link and follow the instructions....
https://github.com/jlhonora/mspgcc-install

**Using MSPGCC with Eclipse**

 1. Install Eclipse
 2. Install c/c++ development plugin  for eclipse.
 3. Create a new c project
 4. In order to use mspgcc compiler you have make following settings in the project

     

 - Right click on the new project folder and select Properties.
 - Under C/C++ Build -> Settings -> Tool Settings you should find information on the compiler, linker and assembler to be used. While the commands should be alright, you might have to do some adjustments to the include libraries.
 - For the compiler these are under includes, /usr/local/msp430/msp430/include
 -  For the linker under Libraries  [Example :In the library search path add   /usr/local/msp430/msp430/lib/ldscripts/cc430f5137 (Give the path depending on what your device is...)  /usr/local/msp430/msp430/lib /usr/local/msp430/lib ]
 - For the assembler under General. 
  /usr/local/msp430/msp430/include
   
   Make sure the locations indicated in these fields match your mspgcc directory.
   
 **Compiling the code**
 
Right click on the project and click on Build project... If there are no errors you should see .hex file in your project folder.

**Installing in Development kit**

Connect the kit to your computer and use the cc430-bsl.py file with the following command.. (If you are using cc430)

sudo python cc430-bsl.py  --surf -c /dev/ttyUSB0 -r -e -I -p [path to your hex file]
