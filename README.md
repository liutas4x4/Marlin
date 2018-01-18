# Fork of Marlin 3D Printer Firmware
<img align="right" src="../../raw/1.1.x/project_specific_files/images/400px-IMG_3896.jpg"/>

## Fork target

For [Acrilyc Geeetech I3 Pro X](http://www.geeetech.com/wiki/index.php/Prusa_I3_X) with IR differential Z probe.

## Clone of GT2560 board

Board looks the same as GT2560, but there are not any printed "GT2560" silkscreen mark. Also, all endstops are 2-pin Molex connectors and for Z steppers there are only one connector, splitted cable is needed. As tested, it is exactly GT2560 rev. A from the side of Marlin.

## Z probe

Idea and schematics of the probe by David Crocker (a.k.a. DC42) 
 - [Mini height sensor board](https://miscsolutions.wordpress.com/mini-height-sensor-board/). Complete description of the board, it's setup and tuning.
 - [Firmware and schematics](https://github.com/dc42/OrmerodSensorBoard). Version V1.0_1.1 is used in this project.
 
PCB is mine: 
 - [Eagle files](https://github.com/liutas4x4/IR-probe_byDC42/tree/master/Eagle_files). Slightly different from DC42, mirrored design.
 - [Gerber files](https://github.com/liutas4x4/IR-probe_byDC42/tree/master/Gerber_files). Based on Sparkfun cam profile for Seeedstudio.
 
Also, holder for this probe is mounted on changed left Geeetech's bracket - part #I3B1-31:
 - [FreeCAD and STLs](https://github.com/liutas4x4/IR-probe_byDC42/tree/master/I3B1-31-Bracket_modified). All files are in open format.

## MK2a Heatbed

Voltage from Geeetech's Power Supply is about 10.9 Volt maximum, and total resistance of MK2a PCB Heatbed, including wires and connector to GT2560 is 1.45 Ohm minimum. Therefore, maximum power of this heatbed is 81.45 Watt. 

So, bedKp and bedKi must to be set to more agressive values.

80 Watt power is not enough to achieve 115-120°C if MK2a is used "as is", especially in cold room or/and with borosilicate glass placed on it. So, in the particular project MK2a is insulated underneath with 1mm cork mat and commecial ("food") aluminium foil.

Please note, that thikness of borosilicate glass, supplied by Geeetech is 3.3mm, not 4.

## Current Status of Fork: In Development

Set of the fork under test is at "GeeetechI3X" branch.
Marlin 1.1.7 is used in this fork.
To current day, Bilinear autoleveling is not working correctly, so

## ToDo

- Working to find mistical crosses of Fade Heght and M851.

## Marlin Resources and Credits

See main [Marlin](https://github.com/MarlinFirmware/Marlin) GitHub directory.

## License, the same as Marlin itself

Marlin is published under the [GPL license](https://github.com/COPYING.md) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.


