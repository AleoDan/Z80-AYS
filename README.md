This project contains schematic, PCB and gerber files for an external sound interface based on AY-3-8910 sound chip, that is 100% software compatible with the ZX Spectrum 128K, +2, +2A, +3, +2B, and +3B models, but with some enhancements to be also hardware compatible with Romanian Home Computers like HC-91 or HC-2000.

These computers were ZX Spectrum compatible RE-DESIGNS and NOT CLONES, because they use very diferent hardware implementation !

The project use some original optimized logic for bus conversion from the Z80 to AY sound chip, so it responds to two ports:

		#BFFD:	write => write selected register contents;	read => read slected register contents;
		#FFFD:	write => select register;					read => read selected register contents;

The interface has a stereo jack output and an on-board mono audio amplifier with monitoring speaker.
The 2 x 8 bit parallel ports of the AY-3-8910 chip are driving some bi-color LEDs for light effects that can be used with or without sound.

The PCB was manually routed, with careful separation and shieldind between the analogic and digital sections; for the analog amplifier a star routing topology was implemented for ground and power lines to avoid any signal copling which could lead to distorsions and oscillations.

Schematic and PCB files are in Altium format, the unified gerber file is in Gerbtool format, but the the individual gerber files are in universal format.
