# What developers need to know:

Download the released .ipa file. Sideload or install it with TrollStore _so you can start a happy jailbreak_.

# Supported development environments:

Compatible with all development environments currently used. debugserver entirely supports debugging of additional processes. 

# Troubleshooting:

If your environment is broken:
1. Restart your phone.
2. Turn on "rebuild jailbreak environment".
3. Turn on "jailbreak".


If you get "Sileo 522 error" try to:
1. Change Sileo's language.
2. Use other Wi-Fi network or cellular data.
3. Restore your iPhone settings.

# What developers need to setup:

1. Configure SSH port 22.
2. Configure SSH root access to be password-free (default: alpine). Unable to repair password temporarily.
3. Run `ssh-copy-id -i $HOME/.ssh/id_rsa.pub root@your-ip-address`.

# Stuff to know about this:

- The current test version only supports iOS 15.0-15.1.1 & A12-A15, M1 chipsets. 

- Rootless jailbreak only supports a few tweaks. Lists of compatible tweaks are available [here](https://docs.google.com/spreadsheets/d/1gf8qiEiyBOO7JzwLJ_OSPXV3Abc7y6hd5w29X9DhifI/edit#gid=1721386642), [here](https://ijsu2i1prt.feishu.cn/sheets/shtcnhioQ4ZL3slxIWXyzF7Y6Vh?sheet=65f81f) and [here](https://github.com/itsnebulalol/ios15-tweaks).
  - Unsupported tweaks need to be updated by their developers to support rootless environments. 

- This version installs Sileo, TrollStore, SSH, libsubstitute, libhooker, Procursus repo, Bigboss repo, etc.

- **If iCloud's storage is full, the permasign will break by restarting the device. It may also lead to some other problems. The current cause is unknown (to be checked)**.

- There is no need to change theos or anything else. What you may need to change is the jailbreak environment path in your code (within the .deb package, the path doesn't need changes).

- Perfect support for `make install`.

- Perfect support for `make uninstall`.

- Perfect support for `make do`.

- No changes are required for iOSOpenDev usage.

- During the jailbreak process, the terminal will display the current log, please ignore it, don't worry if it displays the following: 
```
ldid: Unknown header magic 
Are you sure that is a Mach -O? 
ldid: operator(): No such file or directory
```
> You can ignore this because it doesn't affect the tweak's functionality.
		
- Installing local .deb files are not supported for now.

# Jailbreak main directory:
__/var/jb__. 

Rootless equivalent to the previous directory (this supports third-party APP r/w, which can be used to access data).

## Other directories:
- Fonts: /var/jb/Library/Fonts (fonts can be changed).

- LaunchDaemons: /var/jb/Library/LaunchDaemons.

- Check others: /var/jb/Library/.

# About my daemons:
- **launchdhook** function hook launch. _(can't be terminated)._

- **jailbreak_safe** function can be restarted without exploiting vulnerabilities again. _(can't be terminated)._

- **jailbreakd** function signature and all signing permission related operations. _(can't be terminated)._


# Bugs.
- White icon of known third-party system process (to be solved).

# Changelog.

- 1.1.3.6
 
Fix the issue of usb getting stuck.

Fix sharing file issue.

Fix 1.1.3.5 Applist not working properly.

Fix translation breaking the system.

Fix some possible restart problems.

Fix testflight not updating.

Fix third-party apps injection issues.

---

## To correctly install the newest version, restart the phone and turn on "reinstall the jailbreak environment".
