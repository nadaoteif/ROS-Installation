
# Robot Operating System (ROS) installation and configuration

## Overview:

These tasks is completed by [Nada Oteif](https://sa.linkedin.com/in/nadaoteif) as a part of [Smart Method](https://s-m.com.sa/en/index.html) for Summer training in 2022 at Robotics and AI track.


## Description:

### Task (1) - Install Ubuntu 20.04 & ROS1 noetic on the Virtual box


1. First using following link: https://www.virtualbox.org/wiki/Downloads to install VirtualBox and complete the Setup steps.

2. From https://releases.ubuntu.com/20.04/ install the desktop image that allows you to try Ubuntu without changing your computer at all.

3. Open virtualBox and click on the New button, name your VM then select the location for it to install and complete the setup steps. Then back to main window and select start, browse the file location, then select the ISO file for Ubuntu 20.04. After that click on the Install Ubuntu option then finish the setup steps.

4. On ubuntu go to http://wiki.ros.org/noetic/Installation/Ubuntu then follow the instructions provided using terminal to install of ROS1 noetic and make sure that is successfully running.


--------------------------------------------------------------------------------

### Task (2) - Install Ubuntu 20.04 & ROS2 on the Jetson Nano B01


1. On ubuntu, from this link https://forums.developer.nvidia.com/t/xubuntu-20-04-focal-fossa-l4t-r32-3-1-custom-image-for-the-jetson-nano/121768 .. Download Ubuntu 20.04 that compatible  with Jetson Nano then using this command to extract the  image: ```tar -xvjf Xubuntu-20.04-l4t-r32.3.1.tar.tbz2 ```

2. Next, you need to install the BalenaEtcher tool using this link https://www.balena.io/etcher to flash that image on SD card, then extract the app and operate it.

3. Using BalenaEtcher select the Xubuntu image you have downloaded, select the target device ( SD card ) and click Falsh!

4. Go to SD card folder that you have flashed using ubuntu, navigate to boot folder then extlinux folder, and open the terminal in the same path, type sudo vim extlinux.conf, then you have to add the following line in the extlinux.conf after last line in label primary part: ```FDT /boot/tegra210-p3448-0000-p3449-0000-b00.dtb``` to get output on screen.

5. Now put the SD card in jetson nano, connect it to your device, wait untill the booting process has finished, and complete the basic Ubuntu installation steps.

6. From https://docs.ros.org/en/foxy/Installation/Ubuntu-Install-Debians.html follow the instructions provided using terminal to install ROS2 on ubuntu and make sure that is successfully running.
