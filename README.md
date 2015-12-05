#\#Mac Multi-Tool# Quickstart Guide

***What is it?***

Mac Multi-Tool is a script I wrote that tries to automate many of the tasks involved in creating OS X Install USBs and installing Clover onto new OS X drives.  It also has a few functions built in that aid in mounting EFI partitions and getting partition UUIDs.


***Preparation***

Certain folders will be referenced as such in the following portion:

*/Resources* - will be known as *Resources*

*/Resources/Kexts* - will be known as *Kexts*	


Before you can use this tool successfully, you'll want to have a few things in order:

* You'll need to have a "*Clover vX.X rXXXX.pkg*" installer file located in Resources.
Clover can be downloaded from http://sourceforge.net/projects/cloverefiboot/

* * **NOTE** - You can have multiple Clover installer packages in Resources.
The script just looks for the "Clover" prefix when searching for them.

* You'll need to have a "*config.plist*" located in *Resources*.  This config.plist should have the necessary settings to get YOUR hardware to boot.  The default plist includes these boot flags: `kext-dev-mode=1 dart=0 nv_disable=1 -v`

* * **NOTE** - You can have multiple config plists in *Resources*.  The script just looks for the "*config*" prefix when searching for them.  This feature is helpful if you build installers for several different sets of hardware, you could have *config-mobo1.plist*, *config-mobo2.plist*, etc.

* You'll need to have an "*HFSPlus.efi*" file in *Resources*.
HFSPlus.efi can be downloaded from https://github.com/JrCs/CloverGrowerPro/tree/master/Files/HFSPlus/X64

* * **NOTE** - You can have multiple HFSPlus files in Resources.  The script just looks for the "*HFSPlus*" prefix when searching for them.  I just included this in case a newer version of "*HFSPlus.efi*" emerges that may have some compatibility issues for certain hardware.

* You'll need to have the *.kext* file specific to **YOUR** hardware in *Kexts*.  The script will iterate over all the available files in the *Kexts* folder that end in "*.kext*" and will copy them to the appropriate directory on the target disk, then apply the correct owner/permissions to each.  At some point, I may rewrite parts of the script to allow for other sub folders that could be displayed as a list similar to the items above, that will allow for different kexts for different hardware, but I just haven't yet.

You can find *FakeSMC.kext* bundled with the *HWSensors* at https://github.com/kozlek/HWSensors or http://sourceforge.net/projects/hwsensors/


***Quick Start***

The easiest way to get started with this script is:

* Ensure you have gone through the "***Preparation***" steps above.
* Open the script by double-clicking on "*#Mac Multi-Tool#*"
* Agree to the warning by pressing *[enter]*
* Select option 1 - "*Installer Menu*" at the main menu
* Select option 1 - "*Auto-Create USB Installer*" at the installer menu
* Follow the remaining prompts

* * **NOTE** - Some tasks require an administrator password.


***Advanced Options***

There is an "*Advanced Installer Menu*" option located in the "*Installer Menu*".  This contains all of the individual steps for creating an OS X Installer USB.  If you are at this menu and select the "*?*" option, it will outline what each step does.



***Contact - Questions - Bugs***

If you run into any questions, bugs, or problems with this script, please send me a message on Reddit.

www.reddit.com/u/corpnewt
