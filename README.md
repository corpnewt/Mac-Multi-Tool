#\#Mac Multi-Tool# Quickstart Guide

***What is it?***

Mac Multi-Tool is a script I wrote that tries to automate many of the tasks involved in creating OS X Install USBs and installing Clover onto new OS X drives.  It also has a few functions built in that aid in mounting EFI partitions and getting partition UUIDs.


***Preparation***

Folder Layout:

	+ Script's Parent Folder
		- #El Cap - Win10 Dual Boot#.txt
		- #INFO - READ ME#.txt
		- #Mac Multi-Tool#
		+ Resources
			- Clover vX.X rXXXX.pkg
			- config.plist
			- HFSPlus.efi
			+ Kexts
				- FakeSMC.kext
				- Other Kexts Your HW Requires
		+ Extras
			- #Clover Last Boot Device#.txt
			- #Hiding Clover Partitions#.txt
			- MountEFI
			- Recovery UUID


	Key: - = File
	     + = Folder

Certain folders will be referenced as such in the following portion:

*/Script'sParentFolder/Resources* - will be known as *Resources*

*/Script'sParentFolder/Resources/Kexts* - will be known as *Kexts*	


Before you can use this tool successfully, you'll want to have a few things in order:

1. You'll need to have a "*Clover vX.X rXXXX.pkg*" installer file located in Resources.
Clover can be downloaded from http://sourceforge.net/projects/cloverefiboot/
- NOTE - You can have multiple Clover installer packages in Resources.
The script just looks for the "Clover" prefix when searching for them.

2. You'll need to have a "*config.plist*" located in *Resources*.  This config.plist should have the necessary settings to get YOUR hardware to boot.  The default plist includes these boot flags: `kext-dev-mode=1 dart=0 nv_disable=1 -v`

- NOTE - You can have multiple config plists in *Resources*.  The script just looks for the "*config*" prefix when searching for them.  This feature is helpful if you build installers for several different sets of hardware, you could have *config-mobo1.plist*, *config-mobo2.plist*, etc.

3. You'll need to have an "*HFSPlus.efi*" file in *Resources*.  I cannot distribute that file for copyright reasons, but you can search for it online.

- NOTE - You can have multiple HFSPlus files in Resources.  The script just looks for the "*HFSPlus*" prefix when searching for them.  I just included this in case a newer version of "*HFSPlus.efi*" emerges that may have some compatibility issues for certain hardware.

4. You'll need to have the *.kext* file specific to **YOUR** hardware in *Kexts*.  The script will iterate over all the available files in the *Kexts* folder that end in "*.kext*" and will copy them to the appropriate directory on the target disk, then apply the correct owner/permissions to each.  At some point, I may rewrite parts of the script to allow for other sub folders that could be displayed as a list similar to the 1-3 above, that will allow for different kexts for different hardware, but I just haven't yet.


***Quick Start***

The easiest way to get started with this script is:

1. Ensure you have gone through the "***Preparation***" steps above.
2. Open the script by double-clicking on "*#Mac Multi-Tool#*"
3. Agree to the warning by pressing *[enter]*
4. Select option 1 - "*Installer Menu*" at the main menu
5. Select option 1 - "*Auto-Create USB Installer*" at the installer menu
6. Follow the remaining prompts

- **NOTE** - Some tasks require an administrator password.


***Advanced Options***

There is an "*Advanced Installer Menu*" option located in the "*Installer Menu*".  This contains all of the individual steps for creating an OS X Installer USB.  If you are at this menu and select the "*?*" option, it will outline what each step does.



***Contact - Questions - Bugs***

If you run into any questions, bugs, or problems with this script, please send me a message on Reddit.

www.reddit.com/u/corpnewt
