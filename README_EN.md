#* * What developers need to know**

After you get the tool, you will need to sign the ipa or use Torllstore to install it to your device, so you can start a happy jailbreak

#* * Supported development environments:**

Compatible with all development environments you currently use
Currently, the debugserver perfectly supports the debugging of additional processes (you do not need to do anything)

#* * Environment repair:**

If your environment is damaged, you can restart your phone, turn on the Rebuild jailbreak Environment switch, and then turn on the jailbreak

#* * What developers need to prepare:**
Configure the complete ssh port 22
Configure SSH password free root password on the console (default: alpine)
ssh-copy-id -i $HOME/.ssh/id_ rsa. Pub root @ your ip

#* * Precautions:**
The current test version only supports 15.0-15.1.1 A12-A15-M1. Rootless jailbreak supports some plug-ins. Some unsupported plug-ins need to be updated by the plug-in author to support rootless environments. This version integrates Sileo,TrollStore, ssh, libsubstitute, Libhooker, Procursus, Bigboss, etc

If the storage space of iCloud is known to be full, the permanent signature will become invalid after the space is restarted. It may also lead to some other problems. The current cause is unknown (to be checked)
Since some plug-ins have not been adapted to the current version, please do not update the 35 updates in Sileo for the time being, because it may cause incompatibility and lead to other unknown problems. (Wait patiently for the developer to adapt)
There is no need to change the theos or change anything. What you may need to change is the relevant path in your code (the path in the deb package does not need to be changed, and nothing needs to be changed)
Perfect support for make install
Perfect support for make uninstalll
Perfect support for make do

About the normal use and installation of iOSOpendev, no changes are required

Compile the log. During the compilation process, the console will display the current log. Please ignore it
If the console displays as follows:
ldid: Unknown header magic
Are you sure that is a Mach-O?
ldid: operator(): No such file or directory
You can ignore this warning because it does not affect the normal operation of your Tweak
Install local deb (not supported temporarily)

#* * Jailbreak Directory**
/var/jb
Equivalent to the previous root (this directory supports third-party APP read/write permissions, which can be used for process data interaction)

#* * Font Directory**
/Var/jb/Library/Fonts (fonts can be changed)

#* * Guardian Directory**
/var/jb/Library/LaunchDaemons

#* * Please check other directories**
/var/jb/Library/

#* * About my daemons**
Launchdhook (can't be ended) function hook launch
jailbreak_ safe (non ending) function can be started again without exploiting vulnerabilities
Jailbreakd (cannot be ended) Function signature and all signing permission related operations


If I have more to say, I will update here
