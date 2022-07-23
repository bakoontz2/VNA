This a project to create a Vector Network Analyzer based on the EU1KY antenna tuner that can be reconfigured for different needs.  This material is copyrighted by Daniel Marks (KW4TI) and licensed under the Creative Commons License CC-BY-SA 4.0.  The software is licensed under the zlib license.  These are open source licenses that permit commercial use, modification and redistribution with attribution, and require licensees to assume all risk for using the copyrighted materials.

Currently what is on this github are the Kicad files for the VNA and the software.  The software uses the "stm32duino" extension to the Arduino IDE.  The Arduino IDE can be downloaded from

https://www.arduino.cc/en/Main/Software

The stm32duino software can be installed using the instructions on the stm32duino web site

https://github.com/rogerclarkmelbourne/Arduino_STM32/wiki/Installation

which involves (at this time) downloading the git archive for the stm32duino and placing it under the "hardware" folder in your Arduino folder.

There are several Arduino libraries that are required for the SI5351A frequency synthesizer chip, ILI9341 TFT display module, and XPT2046 touchscreen controller.  These are provided for your use under the "libraries" directory of this archive, but may not be the most recent versions.  You could copy these directories into the "libraries" folder in your Arduino directory.

---------------------------------

The VNA may be used with or without a touchscreen.  If a touchscreen it used, it should be compiled with the "VNA_TOUCHSCREEN" defined in VNA.h.  If you do not have a touchscreen, you can ground the pin PB13 and it will start up without a touchscreen, only appearing a USB CDC serial port device.  You can then type "HELP" to see the list of commands.

The touchscreen used is a 2.8" touchscreen with a SPI interface to the ILI9341 and XPT2046.  These are commonly available at a low price.  To connect it to the SPI interface connector header "J1" on the board, use a 14 pin IDC ribbon cable.

----

The STM32 doesn't ship with an Arduino bootloader installed. Here are some links to get that installed:

* https://m.youtube.com/watch?v=Myon8H111PQ&t=0s 
* https://www.sgbotic.com/index.php?dispatch=pages.view&page_id=48
