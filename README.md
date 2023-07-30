## GrapheneOS OTA update script for rooted firmware

Simple update script for bash to flash OTA updates for GrapheneOS. This update script is **only** for devices using root and Magisk! If your firmware isn't rooted use the built in OTA update shiped with GrapheneOS.

Note that you need to follow the guide how to sign the bootloader with your own keys and apply those steps first. This is **only** for OTA updates! Also don't forget to disable the built in OTA in GrapheneOS, else you might break everything. To turn off the update client, go to Settings ➔ Apps, enabling Show system via the menu and selecting System Update. Then disable the app.

For more information about locking the bootloader with Magisk and root, check the guide on XDA  https://forum.xda-developers.com/t/guide-to-lock-bootloader-while-using-rooted-grapheneos-magisk-root.4510295/

## First steps
This script uses avbroot, you need to clone this first. Then create the directories **ota** and **keys** in the root directory of avbroot.
Put your custom keys you used to sign the bootloader within the keys directory.
Download the latest OTA firmware from GrapheneOS website and put it in the ota directory.
Downoad latest version of magisk and put it in the root directory of avbroot.
Make sure to make the script executable with **chmod u+x ota_update**.

## Usage
Before executing the script, turn on ADB debugging first in Developer Options. Connect your phone to the computer with an USB-cable.
Run the script and select the OTA firmware you want to flash. The script will sign the image with your keys and reboot the phone and fash the OTA.
Wait until the process is done. The phone will then reboot.
