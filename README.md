# Enraged-Taco-test
Multi extruder single hot end mmu.

Multi material printing based off parts I had lying around, this will mainly be how to get this working on the Creality K1, this should also work with the K1 Max. 

DO THIS AT YOUR OWN RISK I'M NOT RESPONSIBLE FOR ANYTHING THAT MAY OR WILL HAPPEN TO YOUR PRINTER!!!!!!!!!!!!!

IF YOU DON'T UNDERSTAND KLIPPER OR ARE UNCOMFORTABLE WITH WORKING ON A PRINTER DO NOT ATTEMPT!!

Parts needed:
4x extruder steppers I used nema17 steppers but others should work as well.
4x extruder mechanism's, I'm using ender 3 v2 mechanisms.
1x usb type c cable or usb to uart cable(not tested)
1x SKR pico with klipper flashed to it. Using voron mount for the pico.
1x rooted K1/K1 Max.
1x filament splitter, I used one from thingiverse from the Bambu labs A1
4x or more ptfe guide tubing.
16ga wire to power the skr pico.
A way to manage filament, I'm using the carrot patch from the enraged rabbit carrot feeder.
A mounting system for the extruders as well the filament buffers. I'm using 2020 extrusion with a self designed mount for the steppers.
A way to join together the extrusions, I'm using the ercp extrusion mount file from the user mods section.
A way to lift extrusion off a surface to make room for steppers as well as other items.

That is what I have into this so far.

First thing is getting the Pico to talk to the K1 as well as supplying power to the pico from the K1(remove bottom cover and tap into open slots on the power supply), in order to do so you will need root as we need to ssh in order to grab the uart address that is assigned by the K1. Use command dmesg and look for new device and its tty its been asigned.

Once thats established, create a new .cfg file and copy my config and edit as needed for your setup. Also add the include <yourconfigfile>.cfg in the main printer.cfg. Save and restart, you should not have any issues if you do make sure the tty added to the printer.cfg is correct for the pico.

Next add my other cfg file that handles tool changes, this has macros as well as how the printer handles syncs with the main extruder.

Included in this will also be a .3mf file with my slicer config for mmu printing on the K1, I use tip forming until a cutter is developed this is what I'll use for now.

At this time I have the rear filament run out sensor disconnected and running one on the tool head but it is currently disabled until I or another user gets a good macro set up for it.

Links to all parts will be posted later.

THIS IS MY FIRST GIT HUB THING SO LET ME KNOW WITH KINDNESS WHAT I GOOFED :)
