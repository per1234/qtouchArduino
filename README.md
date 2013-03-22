qtouchArduino
=============

Arduino library for the Atmel QT1110 chip: http://www.atmel.com/images/doc9520.pdf

To set up the chip:

Basically, hook up power and gnd, and put a .1uF cap across them (near the chip).  
Then hook up the SPI:
MISO arduino pin 12 -> QT1110 pin 16, 
MOSI arduino pin 11 -> QT1110 pin 15,
SCK arduino pin 13  -> QT1110 pin 17, 
SS (your choice, often arduino pin 10, or mega pin 53 -> QT1110 pin 14).    

Now, you need to hook up a touch plate.  I just soldered a wire to an unetched PCB board (I used one that was about 2cm square).  Put that into 4.7k resistor.  From there put a 20nF (or so) cap to pin 2.  And put a wire from the resistor to pin 3.  Check the QT1110 datasheet for the other cap sensing wire pairs.

Use this revision of the library if you are on pre 1.0.4 Arduino.  See: http://code.google.com/p/arduino/issues/detail?id=888
