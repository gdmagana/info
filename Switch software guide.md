I currently installed this microsd in your switch. It's a solid one for just doing large reads of game files, but it isn't quite as nice as a SanDisk brand 1tb card.
![[Pasted image 20250525144033.png]]

your old 128gb should not be considered sufficient, as creating emulated OS environments (emuMMCs) and other backups can take upwards of 30GB each. I would recommend a 256 or 512 GB microsd card, which can be found for about $20 and $40 respectively.

Main guide followed for activating homebrew:
https://switch.hacks.guide

### HOW TO INSTALL A GAME:
- Ask Gabe or another reputable source for a legally, ethically, etc. obtained copy of the particular game you desire :)
- I use [ns-usbloader](https://github.com/developersu/ns-usbloader) on macos, but it has release version for windows/linux. it contains many tools. you may need to install a specific JDK, read the install instructions.
- ![[Pasted image 20250611200536.png]]This window can be used to select switch game files (\*.nsp, \*.xci, \*.nsz) and upload them to a game installer on the switch (use Awoo installer, yes the one with anime catgirl).
- To open up Awoo on your switch, launch a game and hold down the R shoulder button. Then, select Awoo from your list of homebrew apps. Select "Install over USB". Let me know if this method doesn't work for your setup; with my old switch it was finnicky and i resorted to installing things by moving the files onto the SD card first.
	- ![[Pasted image 20250611202630.png]] If you do need to move a large file onto your SD Card, you need to split it up into 4GB chunks, which you can luckily do with this tab of ns-usbloader
### HOW TO REBOOT YOUR SWITCH INTO HEKATE OR HOMEBREW 
- ![[Pasted image 20250611200726.png]]
- This page is used to inject a payload whenever the switch is in Recovery mode. To get to recovery mode, you need to use the RCM jig and follow [these instructions.](https://switch.hacks.guide/user_guide/rcm/entering_rcm.html) Gabe's full method is as follows:
	1. With the switch on, hit the power button once to put it to sleep. Plug it into your computer, this should charge the switch. (If you plug it in with it on, it might try to charge ur computer)
	2. Make sure the R joycon is slid all the way in
	3. Hold the power button for a few seconds, select power options, Turn Off
	4. Your switch is now off. Slide out the right joycon, replace it with the RCM jig.
	5. Hold the volume up button down
	6. While holding volume up, press down the power button for about one second. You should now be in RCM
	7. With the switch in RCM, you can now inject the hekate or fusee payload using NS-USBloader. 
		- fusee should take you straight to your homebrew-ed switch software, while hekate is like a launcher layer that contains many tools for managing your custom firmware and backups. i normally launch hekate and then hit payloads > fusee.bin to launch the switch back to where i want it.