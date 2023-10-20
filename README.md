## BOSSA 1.9.1

BOSSA is a flash programming utility for Atmel's SAM family of flash-based ARM microcontrollers. The motivation behind BOSSA is to create a simple, easy-to-use, open source utility to replace Atmel's SAM-BA software. BOSSA is an acronym for Basic Open Source SAM-BA Application to reflect that goal.

The software was created by Scott Shumate with contributions from several contributors.

The software is released under the terms of the BSD license as specified in the LICENSE file


1 - git clone  --recurse-submodules https://github.com/wxWidgets/wxWidgets.git

2 - sudo apt-get install libgtk-3-dev build-essential checkinstall
  * $./configure
  * $make
    
3 - Excute these commands
	* $cd include/
	* $sudo cp -Rf wx /usr/include/.
	* $sudo cp /usr/local/lib/wx/include/gtk3-unicode-3.3/wx/setup.h /usr/include/wx/.
 
4 - export LD_LIBRARY_PATH=/usr/lib:/usr/local/lib:/lib

5 - Excute these commands
	* $sudo apt-get install build-essential
	* $sudo apt-get install libwxbase3.0-dev
	* $sudo apt-get install libwxgtk3.0-gtk3-dev
	* $sudo apt-get install libreadline-dev
	* $sudo apt install libwxgtk-webview3.0-gtk3-dev
6 - Correct in Makefile the WXVERSION for the version you installed.
    VERSION?=$(shell git describe --tags --dirty)
    WXVERSION=3.3

7 - sudo update-alternatives --config wx-config 
    Select: * 0            /usr/lib/aarch64-linux-gnu/wx/config/gtk3-unicode-3.0   309       auto mode	
	
8 - make bossac or make -j

9 - The program will appear in ./bin
