# BIGTREETECH Pad5 V2.0 with Orange Pi CM4

[Orange Pi Compute Module 4](http://www.orangepi.org/html/hardWare/computerAndMicrocontrollers/details/Orange-Pi-CM4-1.html) is an inexpensive RK3566 board, pin-compatible with Raspberry Pi CM4. It works with most third-party carrier boards that are designed for RPI CM4.

Armbian has a board profile for Orange Pi 3B (`orangepi3b`), which is quite identical to CM4, just in a different packaging. 

[BIGTREETECH Pad5 V2.0](https://github.com/bigtreetech/Pad5/tree/master/Pad5-V2.0) is a carrier device for RPI CM4/CM5, providing a 5-inch 800×480 LCD screen with a bunch of peripherals.

The Pad5 manual mentions that USB3.0 is only available for CM5. In my tests, the two USB3.0 ports did not even react on plugging in devices.  The two USB2.0 ports worked fine. The USB-C port provides power and access to the built-in USB-Serial adapter. 

The device boots directly from the MicroSD card if it's inserted.

The desktop version of Armbian works fine on the device. Touchscreen works out of the box. Wifi and Bluetooth work on CM4, provided that you attach an external antenna.

The Pad5 manual says that the power button works only for CM5, but it kinda works in this setup. Be aware that it just abruptly power-cycles the board.

External HDMI port on the Pad5 does not work, although Armbian supports it (tested by plugging the CM4 into a standard CM4 carrier board).

Under stress tests (using `strtess-ng --all 4`) the CPU survives without a heatsink, reaching 85C. Probably, a heatsink would still be nice.

