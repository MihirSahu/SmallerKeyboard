# QMK Smallerkeyboard

This is for archiving my first experience with the keyboard and is not meant to be used as a projct.
<br>
This was used to build 2x2 keyboards on a pro micro with QMK.
<br>
## Instructions
<br>
1.	Install QMK MSYS and qmk_toolbox
<br>
2.	Extract the contents of smallerkeyboard.zip to C:\Users\<username>\qmk_firmware\keyboards
<br>
3.	Edit the keymaps in C:\Users\<username>\qmk_firmware\keyboards \smallerkeyboard\keymaps\default\keymap.c to whatever you want (see keycodes here https://docs.qmk.fm/#/keycodes_basic)
<br>
4.	Open QMK MSYS
<br>
5.	Use “qmk setup” and follow installation
<br>
6.	Use  qmk compile -kb smallerkeyboard -km default (Change if you’re using different path or keyboard layout)
<br>
7.	Now there should be a .hex file in the format <keyboard name>`_`<keyboard layout> in in C:\Users\<username>\qmk_firmware. My file is called smallerkeyboard_default.hex
<br>
8.	Now launch qmk toolkit and load up the .hex file we compiled. Then select the “Auto-Flash” option
<br>
9.	Connect the pro micro controller to the pc and short the GRD and RST pins (I had no idea what this meant so I had to do some digging. I tried using a paperclip but it didn’t seem to be metal and it didn’t work. I then tried using pins that came with my Arduino digisparks but it didn’t work and I ended up poking myself fingernails 3 times. Finally, I used a staple and it worked perfectly). Qmk toolkit will automatically detect it and flash it
<br>

