Arduino Mini Pro clone with Atmega328PB, Barco Edition

This is basically an Arduino Mini Pro clone but with an Atmega328PB instead of Atmega328P.
The generic components that are needed when modding Barco ADVM monitors have been added
to make the mod "prettier".

Speed 16MHz and 5V.

The reasoning is to have the secondary I2C controller of the PB version, thus PE0 and PE1
pins are pulled to 2.54mm THT holes just like A4/A5 pins of the primary I2C controller.
These are then connected to the buffer already so no extra breakout PCB and intermediate
resistors are needed.

It is still recommended to add a 100R resistor to SDA and SCL lines right at the pads of
the original resistors on the signal PCB.

Remember to burn a bootloader and fuses with a *real* programmer (like another Arduino
turned into an ISP). This requires you to connect to the ICSP pins, MOSI, MISO, SCK,
RESET, 5V and GND. I used a male pin header row  which I didn't solder but just held in
place during programming.

(2024) Martin Hejnfelt, martin@hejnfelt.com


