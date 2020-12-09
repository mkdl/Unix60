# Unix60
The Unix60 is a budget FR4 keyboard designed to make a HHKB-style layout available to everyone with as few compromises as possible.


![Image of Unix60 Top](Pictures/Top.jpg)

![Image of Unix60 Back](Pictures/Back.jpg)

![Image of Unix60 Decal](Pictures/Decal.jpg)

![Image of Unix60 Plate](Pictures/Plate.jpg)

![Image of Unix60 PCB](Pictures/PCB.jpg)

![Image of Unix60 Case](Pictures/Case.jpg)

If you have any questions or need help, please join the FR4 Discord: https://discord.gg/z7mpQX5YJQ

### Disclaimer: You must follow this guide in the order it is written. Assembling stuff in the wrong order (specifically your Pro Micro or Elite C and its headers) will likely result in you having to desolder components and significantly increase the amount of time it takes to assemble. I am not responsible for boards damaged during assembly. I highly recommend you read through the entire guide before starting assembly.

# Assembly:

### 1. Put the diodes through the PCB so the legs stick out the front side of the board and so the diode is flush with the back, making sure the black line on the diode faces the square pad:
![Image of diode in PCB](Pictures/1.jpg)
### 2. Solder from the back and snip the legs:
![Image of soldered diode](Pictures/2.jpg)
### 3. Place your Pro Micro or Elite C onto its pin headers and sit it into the board so the Pro Micro is on the back of the PCB (the side with the Unix60 logo) and tape it down to temporarily hold it in place. This helps align the pin headers properly. It doesn't matter whether you put the shorter pins on the PCB or the longer ones; either way, you will have to snip the longer ones once you've soldered them in. **DO NOT SOLDER THE PRO MICRO OR ELITE C TO THE PIN HEADERS YET!**
![Image of taped Pro Micro](Pictures/3.jpg)
### 4. Solder in the pin headers from the front side of the PCB. **Do not solder the Pro Micro or Elite C yet, just the headers!**
![Image of soldered headers](Pictures/4.jpg)
![Image of soldered headers](Pictures/5.jpg)
### 5. Solder your reset button to the PCB 
![Image of soldered diode](Pictures/6.jpg)
### Note: If you've lost your reset button, don't worry. Shorting the two pads closest to the edge of the PCB or the two closest to the inside will reset your controller. After all, that's all the button does :)
### 8. Attach your stabs to the PCB (do not be afraid to push, you won't break it)
![Image of soldered headers](Pictures/7.jpg)
### 9. Mount switches in the corner of the plate to align it, then lower the plate onto the PCB
![Image of soldered headers](Pictures/9.jpg)
### 10. Add the rest of your switches and solder them all in
![Image of soldered headers](Pictures/10.jpg)
### 11. Once you have verified that all your diodes, switches, and Pro Micro or Elite C pin headers are soldered properly, you can now solder your Pro Micro or Elite C onto the pin headers:
![Image of soldered Pro Micro](Pictures/11.jpg)
### 12. Attach standoffs to the bottom of the plate using screws from the other side
![Image of soldered headers](Pictures/12.jpg)
### 13. Screw on the bottom plate
# Flashing instructions for Linux:
### 1. Plug your Pro Micro or Elite C in
### 2. Open up the [QMK configurator](https://config.qmk.fm/#/FR4/Unix60/LAYOUT) and create your desired layout
### 3. Download the .json file (on the left, next to keymap.json)
### 4. Open up a command line
### 5. Type ```qmk flash /path/to/layout.json``` (obviously replacing the file path with the path to your downloaded layout) and follow any additional instructions
### One thing to note is that you can compile a .hex file on the configurator and flash that with avrdude, however, I prefer the method outlined above.
# Flashing instructions for Windows:
### Please keep in mind that I do not run Windows on my own system and cannot 100% verify this flashing procedure will work or if it requires any other configuration. I highly recommend you check the QMK docs if something is not working. 
### 1. Plug your Pro Micro or Elite C in
### 2. Open up the [QMK configurator](https://config.qmk.fm/#/FR4/Unix60/LAYOUT) and create your desired layout
### 3. Click "compile" in the upper right, and once it's done, download the .hex by clicking "firmware"
### 4. Open up QMK toolbox and load your downloaded .hex
### 5. Click "flash" and follow any additional instructions
