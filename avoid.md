# Tips about what not to do with your installed system

More information: https://forum.endeavouros.com

## Do not favor a GUI package manager over `pacman` or `yay`

A GUI package manager may be nice to use for a user unfamiliar with tools like `pacman` or `yay`.<br>
However, it is best to use `pacman` (or `yay`) to
- install
- update
- uninstall

 packages because
- they have been proved to be more reliable than GUI package managers
- they can provide additional and essential details about the install or update process, which GUI managers do not provide

Thus learning to use `pacman` is important and strongly recommended in EndeavourOS.

If you are familiar with a command line package manager from another distro, see https://wiki.archlinux.org/title/Pacman/Rosetta to get an idea how it compares to `pacman`.

## Do not uninstall "unnecessary" packages without thorough investigation

Trying to uninstall packages that *seem* unnecessary may lead to various problems, e.g. unable to boot the system, or some programs behaving incorrectly.

In other words, do not uninstall any package unless you have thoroughly investigated that the package is not needed by any other program in your system. Note that many packages have dependencies which may complicate the investigation.

Useful investigation tools are e.g.
- `pactree` (<small>package `pacman-contrib`</small>)
- `pacman`

As a rule of thumb, don't uninstall a package if you are not sure if it may be needed.

## Do not let the package cache fill up the disk

The package cache (a folder where older versions of downloaded package files are stored) will eventually fill up the disk partition unless properly managed. A full (or nearly full) partition will cause lots of problems.

To manage the cache, you can manually remove the oldest package files (or those that are no more installed) with the `paccache` command.<br>Or, you can use the `paccache-service-manager` to manage it automatically.

## Do not use AUR packages carelessly

By default, there are basically two kinds of packages:
- official
- AUR

(Here we do not consider flatpaks or snaps although they are available as well.)

The *official* packages are maintained and supported by the Arch and EndeavourOS **teams**, so they should be considered reliable.

The *AUR* packages are maintained and supported by the **community**. This means the Arch and EndeavourOS teams cannot directly control the contents of the AUR packages.
Users should check the contents of an AUR package before usage, and may/should report about problems. Then the Arch team can decide what to do with the package.

However, although most AUR packages can be considered reliable, checking the contents for issues is *strongly* recommended.

An AUR package can be useful if a similar official package is not available. For example, some drivers or special apps are not available in the official repositories.

## Do not use `grub-customizer`

`grub` is one of the available bootloaders, and `grub-customizer` is a graphical settings manager for `grub`. Usage of `grub-customizer` has caused several serious problems, e.g. made the system unable to boot.<br>
EndeavourOS does *not* install it by default, and recommends against installing it.

