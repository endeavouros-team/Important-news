# Known issues

Last update: 2021-Sep-21.

Here we will list known issues of the latest EndeavourOS ISO, drivers and apps.

## ISO

Description of the issue | Possible remedy
:---- | :----
Community editions (sway and bspwn)<br> cannot be installed simultaneously | Install one of them using the ISO, and the other one later.<br>[See forum discussion.](https://forum.endeavouros.com/t/install-both-the-community-editions)
Installer says there is no internet connection,<br> but it does exist. | Using VPN may help, depending on your location.

## Apps

Description of the issue | Possible remedy
:---- | :----
An app behaves unexpected | Make sure your system is properly updated (use terminal command `pacman -Syu` or `yay`).<br>Make sure you have carefully checked and merged all app configuration updates.<br>Use terminal command `eos-pacdiff` for this.
On nvidia system, after system update<br>the next boot stops at a blank screen | Typically, on a kernel update the corresponding nvidia driver package should be updated as well.<br>Sometimes that doesn't happen, which leads to this problem.<br>Remedy: use apps `UpdateInTerminal`, `eos-welcome` or `eos-update-notifier`<br>for updating the system, because they can detect such a problem and let you decide what to do.

## Drivers

Description of the issue | Possible remedy
:---- | :----
Wired (ethernet) connection does not work properly | If you have an `r8168` ethernet card, either uninstall the r8168 package, or reinstall it. Then reboot.