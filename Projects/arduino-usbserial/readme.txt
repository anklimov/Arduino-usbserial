Complete source code to compile ArduinoCore-sam/firmwares/atmega16u2/arduino-usbserial with fixes (*)

Challenge:
Original code require ancent non - release verfion of LUFA framework to be compiled

How to reach it:
git clone https://github.com/abcminiuser/lufa.git  
git reset --hard f6e1eaba7548bce84ae25718d7c37479c4bb0065

then copy ArduinoCore-sam/firmwares/atmega16u2/arduino-usbserial
to Projects/arduino-usbserial

All actions are done in this repo

to compile

cd Projects/arduino-usbserial
make


use Arduio programmer to flash hex file

====
old readme

To setup the project and upload the Arduino usbserial application firmware to an ATMEGA32U2 using the Arduino USB DFU bootloader:
1. unpack the source into LUFA's Projects directory
2. set ARDUINO_MODEL_PID in the makefile as appropriate
3. do "make clean; make"
4. put the 32U2 into USB DFU mode:
4.a. assert and hold the 32U2's RESET line
4.b. assert and hold the 32U2's HWB line
4.c. release the 32U2's RESET line
4.d. release the 32U2's HWB line
5. confirm that the board enumerates as "ATmega32u2"
6. do "make dfu" (OS X or Linux - dfu-programmer must be installed first) or "make flip" (Windows - Flip must be installed first)

Check that the board enumerates as "Arduino Mega 2560".
Test by uploading a new Arduino sketch from the Arduino IDE.
