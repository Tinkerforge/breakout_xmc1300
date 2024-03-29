XMC1300 Breakout
================

This repository contains the firmware source code and the hardware design
files. The documentation generator configs can be found at
https://github.com/Tinkerforge/generators

Repository Content
------------------

software/:
 * examples/: Examples for all supported languages
 * build/: Makefile and compiled files
 * src/: Source code of firmware
 * generate_makefile: Shell script to generate Makefile from cmake script

hardware/:
 * Contains kicad project files and additionally schematics as pdf

datasheets/:
 * Contains datasheets for sensors and complex ICs that are used

Hardware
--------

The hardware is designed with the open source EDA Suite KiCad
(http://www.kicad.org). Before you are able to open the files,
you have to install the Tinkerforge kicad-libraries
(https://github.com/Tinkerforge/kicad-libraries). You can either clone
them directly in hardware/ or clone them in a separate folder and
symlink them into hardware/
(ln -s kicad_path/kicad-libraries project_path/hardware). After that you
can open the .pro file in hardware/ with kicad and from there view and
modify the schematics and the PCB layout.

Software
--------

To compile the c code we recommend you to install the newest CodeSourcery arm
eabi gcc compiler
(http://www.codesourcery.com/sgpp/lite/arm/portal/subscription?@template=lite).
You also need to install bricklib (https://github.com/Tinkerforge/bricklib)
and brickletlib (https://github.com/Tinkerforge/brickletlib).
You can either clone them directly in software/src/ or clone them in a
separate folder and symlink them into software/src/
(ln -s bricklib_path/bricklib project_path/software/src/).

After that you can generate a Makefile from the cmake script with the
generate_makefile shell script (in software/) and build the firmware
by invoking make in software/build/. The firmware (.bin) can then be found
in software/build/ and uploaded with brickv (click button "Flashing"
on start screen).
