# ST-IKBD-RTC

Arduino Nano / ATMega256PU + DS3231 based RTC injector for Atari STf/e.

This module can be used to overcome the ST's IKBD real time clock/calendar limitation to year 1999 and lack of battery back-up. This simple circuit can be plugged between the maotherboard and keyboard, and is completely transparent for the user. It emulates original IKBD clock, so doesn't need any additional drivers nor software. It intercepts communication between keyboard and motherboard, and when clock/calendar related commands are detected it masks them out and supplies own replies. It causes only a minor delay (1.3ms) for keyboard/joystick/mouse signals. As both TOS and Atari Control Panel suprisingly are Y2K compilant (due to kind of bug in bin<->bcd conversion routines), no software patches are required.
