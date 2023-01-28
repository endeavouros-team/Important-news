# Tips about what not to do with your installed system

More information: https://forum.endeavouros.com

## Do not uninstall "unnecessary" packages without thorough investigation

<small>

Trying to install packages that *seem* unnecessary may lead to various problems, e.g. not able to boot the system.<br>
In other words, do not uninstall any package unless you have thoroughly investigated that the package really is not needed by any other program.

Note that many packages have dependencies which may complicate the investigation.<br>
Useful investigation tools are `pactree` (from package `pacman-contrib`) and `pacman`.

</small>

## Do not let the package cache fill up

<small>

The package cache (a folder where older versions of downloaded packages are stored) will eventually fill up the disk partition unless properly managed. A full (or nearly full) partition will cause lots of problems.

To manage the cache, you can manually remove the oldest package files (or those that are no more installed) with the `paccache` command.<br>Or, you can use the `paccache-service-manager` to manage it automatically.

</small>

## Do not use AUR packages carelessly

<small>

By default, there are basically two kinds of packages:
- official
- AUR

(Here we don't consider flatpaks or snaps, although they are available as well.)

The *official* packages are maintained and supported by the Arch and EndeavourOS **teams**, so they should be considered reliable.

The *AUR* packages are maintained and supported by the **community**. This means the Arch and EndeavourOS teams cannot directly control the contents of the AUR packages.
Users should check the contents of an AUR package before usage, and may/should report about problems. Then the Arch team can decide what to do with the package.

Note however that although most AUR packages can be considered reliable, checking the contents for issues is strongly recommended.

An AUR package can be useful if a similar official package is not available. For example, some drivers or special apps are not available in the official repositories.

</small>

