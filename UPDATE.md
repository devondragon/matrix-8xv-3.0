#Updating the Firmware and Key Mappings

The Matrix is a bit unusual, in that it doesn't support VIA or QMK (as far as I am aware).

If you want to update the key mappings, or update the firmware, or both, this is what you need to do.

**1)** You need to use the IATKB online QMK tool.  You should use Chrome or Edge browsers, and go here:

[Matrix @ IATKB](http://iatkb.com/#/8xv3/LAYOUT_default) 

The keyboard should already be selected as "8xv3", if not, please select that.  

**2)** Then click the "Load Default" button to the right.  

**3)** Keymap customization
If you already have a custom keymap JSON file from having done this already, you can load it in now using the green and white icon with the arrow pointing up, immediately the right of the KEYMAP.JSON button in the center just below the output window.  If not, don't worry about it.  

You can customize the key map just like in normal QMK or Via.

Pay attention to F13 and F24.  By default they are mapped to Layer 1 (MO(1)) F1 and F12.  F13 is used to mount the Boot drive for firmware updates and F24 is used to mount the Screen drive for setting the animated image on the Eye screen.  

**4)** When you are done, click the green Compile button near the top right of the screen.

It should output some information in the black output window, and show you a Done message.  

**5)** Next, click the Keymap JSON download button, the down arrow just to the left of the KEYMAP.JSON button.  NOT the KEYMAP ONLY button on the far left (which doesn't seem to work).  This will download the keymap JSON file you can use next time so you don't have to re-do your keymap changes.  So save this file away somewhere safe.

**6)** Next, click the Firmware download button.  It is on the far right, just below the output window. That will download a file named 8xv3.uf2.  This is your new firmware and keymap file, which we will load onto the keyboard.

**7)** If all those goes well, press F13 (function + F1 is the default).  Your keyboard will disconnect, and a USB drive will mount on your computer named BOOT.  

**8)** Copy the 8xv3.uf2 file unto that BOOT drive.  Once it has completed copying, eject the BOOT drive from your OS.  
The keyboard should restart itself, and now has the latest firmware and your custom keymap in place.

