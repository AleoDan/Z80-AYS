![](Z80-ays_top.jpg)
![](Z80-ays_bot.jpg)

This project contains schematic, PCB and gerber files for an external sound interface based on AY-3-8910 sound chip, that is 100% software compatible with the ZX Spectrum 128K, +2, +2A, +3, +2B, and +3B models, but with some enhancements to be also hardware compatible with Romanian Home Computers like HC-91 or HC-2000.

These computers were ZX Spectrum compatible RE-DESIGNS and NOT CLONES, because they use very diferent hardware implementation !
All HC computers have very stable system clock output on the extension connector, so the sound inteface uses this clock divided by two and don't need another on-board oscillator.

The project make use of some original optimized logic for bus conversion from the Z80 to AY sound chip, so it responds to two ports:

		#BFFD:	write => write selected register contents;	read => read slected register contents;
		#FFFD:	write => select register;					read => read selected register contents;

Unlike on the original ZX Spectrums, these ports are better decoded and have only four aliases on the lower half of the address bus, so that they do not overlap over some non-standard ports which HC computers have.

The interface has a stereo jack output compatible with Melodik standard and an on-board mono audio amplifier with monitoring speaker.
The 2 x 8 bit parallel ports of the AY-3-8910 chip are driving some bi-color LEDs for light effects that can be used with or without sound.

The PCB was manually routed, with careful separation and shielding between the analogic and digital sections; for the analog amplifier's ground and power traces a star routing topology was used, to avoid any signal coupling which could lead to distorsions and oscillations.

Schematic and PCB files are in Altium format, the unified gerber file is in Gerbtool format, but the individual gerber files are in universal format.
