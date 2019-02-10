# ST-IKBD-RTC

Arduino Nano / ATMega256PU + DS3231 based RTC injector for Atari STf/e.

This module can be used to overcome the ST's IKBD real time clock/calendar limitation to year 1999 and lack of battery back-up. This simple circuit can be plugged between the maotherboard and keyboard, and is completely transparent for the user. It emulates original IKBD clock, so doesn't need any additional drivers nor software. It intercepts communication between keyboard and motherboard, and when clock/calendar related commands are detected it masks them out and supplies own replies. It causes only a minor delay (1.3ms) for keyboard/joystick/mouse signals. As both TOS and Atari Control Panel suprisingly are Y2K compilant (due to kind of bug in bin<->bcd conversion routines), no software patches are required.

* on STf(m) with TOS 1.00 - 1.04 it works using ST Control Panel (CONTROL.ACC), Panel is used both for synchronizing ST Clock with IKBD Clock on reboot and for manually adjusting the clock,
* on STe with TOS 1.06/1.62 using STE_FIX.PRG and STE Control Panel (CONTROL.ACC), STE_FIX is used for synchronizing ST Clock with IKBD Clock on reboot, Panel is required only for manually adjusting the clock,
* on STe with TOS 2.06 it works using XControl (XCONTROL.ACC), ST Clock with IKBD Clock on reboot synchronization is done by TOS itself, Panel is required only for manually adjusting the clock.
