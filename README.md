# EndeavourOS software news

[![Maintenance](https://img.shields.io/maintenance/yes/2024.svg)]()

## Description of this page

Up to date news for the users of the EndeavourOS software, like
- manual interventions
- important code changes
- ISO releases

and more.

## Useful links

[EndeavourOS forum](https://forum.endeavouros.com) is the official place to talk about EndeavourOS.<br>
[Download the latest ISO](https://endeavouros.com)<br>
[Known issues](known_issues.md)<br>
[General tips](general-tips.md)<br>
[Tips for the EOS apps](tips-for-eos-apps.md)<br>

## Important news

Date<br>yyyy.mm.dd | Description | Additional remarks | Relates to
:--- | :--- | :---- | :---
2024.09.14 | `yay` does not work after the latest of pacman to 7.0.0, and here's a [workaround](https://forum.endeavouros.com/t/pacman-7-0-0-r3-g7736133-1-update). For `paru` we unfortunately need to wait for a solution.<br><br>Update 2024-09-15: the new version (12.3.5-2) of `yay` is OK now.<br><br>Update-2 (2024-09-15): the latest version of `yay` is working again. A temporary workaround for `paru` is to use `paru-git` until upstream `paru` gets fixed.<br><br>Update-3 (2024-09-16): a fixed `paru` has been released to the [endeavouros] repo! | 2024-09-16: *fixed* | pacman 7.0.0, yay, paru
2024.07.02 | OpenSSH security update info for version 9.8p1, [read this!](https://forum.endeavouros.com/t/the-sshd-service-needs-to-be-restarted-after-upgrading-to-openssh-9-8p1) | | Security
2024.07.01 | The latest EndeavourOS ISO is called **Endeavour**! | [Announcement](https://forum.endeavouros.com/t/our-fifth-anniversary-the-return-of-arm-and-the-endeavour-release-with-plasma-6-1-is-here)<br>[Download](https://endeavouros.com/#Download)| ISO
2024.06.12 | The **r8168** driver package is no more supported by Arch. This means users should use the r8169 driver from the kernel, it should work in most cases. See also [this link](https://forum.endeavouros.com/t/the-r8168-driver-package-is-removed-from-arch-repository). | The r8168 package in AUR is orphaned currently. | Realtek 8168 network card
2024.05.11 | Issues with Nvidia 550 drivers, see [this post](https://forum.endeavouros.com/t/nvidia-550-drivers-causing-hard-crashing-during-updates). || Nvidia GPU
2024.04.23 | Meet **Gemini**, the latest EndeavourOS ISO, released today!<br>Here's the [announcement](https://forum.endeavouros.com/t/plasma-6-with-wayland-or-x11-option-and-qt-6-ported-calamares-meet-gemini) and [download](https://endeavouros.com/#Download) page. || ISO
2024.04.09 | The Endeavouros **ARM** installer will be removed from the next ISO. See [this announcement](https://forum.endeavouros.com/t/goodbye-endeavouros-arm) for more info. ||ARM
2024.04.02 | A backdoor was found in upstream package **xz**, update your system *now*! [More info](https://forum.endeavouros.com/t/the-upstream-xz-repository-and-the-xz-tarballs-have-been-backdoored/53253).| | security
2024.01.26 | `eos-pacdiff` supports option<br> `--backup`<br>that makes a backup of the old version of the file.<br>More info: see [this](https://forum.endeavouros.com/t/eos-pacdiff-news/50426) forum post.| | eos-pacdiff<br>file backup
2024.01.09 | If **wayland** does not start properly *and* **x11** works as expected, check your `~/.bash_profile` file. If it contains contains command `exec startx`, remove that line (and the surrounding `if...fi` statement). [See this forum thread](https://forum.endeavouros.com/t/wayland-not-working-by-default-on-an-offline-install/49755).||wayland
2023.09.01 | The implementation about informing the user about recommended reboot after updates has changed. To enable this feature, you need to enable the related systemd service:<br>`systemctl enable --now eos-reboot-required.timer` | Implementation change | Recommended reboot notification on updates
2023.08.16 | The `UpdateInTerminal` app will be removed during this month. Recommended alternatives: `eos-update`, `yay`, or `paru`.<br>The *info page* of UpdateInTerminal has already been removed from package `eos-apps-info`. | `eos-apps-info` for more help. | UpdateInTerminal
2023.05.23 | EndeavourOS *keyring* package has been updated. If you have problems updating your system, you may need to update the `endeavouros-keyring` package first, then other packages:<br>`sudo pacman -Sy endeavouros-keyring; sudo pacman -Syu`<br>Alternatively, you can use command<br>`eos-update` | [See more](https://forum.endeavouros.com/t/endeavouros-keyring-updated-users-should-update-soon/41117)
2023.05.04 | Python 3.11 update has caused various issues, see [here](https://forum.endeavouros.com/t/users-of-optimus-manager-beware-the-python-update/40379) and [here](https://forum.endeavouros.com/t/the-python-3-11-rebuild-has-arrived-expect-a-large-number-of-updated-packages/40363).
2023.03.30 | Updated ISO, [Cassini Nova R1](https://endeavouros.com/latest-release), includes updated packages, e.g. the latest Nvidia 530 series driver. | Latest Nvidia driver | ISO
2023.03.25<br>2023.03.18 | The EndeavourOS ISO might not boot with the latest Nvidia cards. See [this workaround](https://forum.endeavouros.com/t/latest-nvidia-cards-do-not-boot-installer-liveiso/38650/1) and [the new weekly ISO at 2023.03.24](https://forum.endeavouros.com/t/latest-nvidia-cards-do-not-boot-installer-liveiso/38650/19). | Workaround | Nvidia & ISO
2023.03.13 | Kernel update problems, see this: https://forum.endeavouros.com/t/heads-up-on-latest-kernel-update-6-2-5-arch1-1/38399 | Affects some users | Kernel issues
2023.03.08 | ISO release: [Cassini Nova](https://endeavouros.com/latest-release) || ISO
2023.02.26 | Package `grub-customizer` is an app that causes lots of help requests in forums.<br>Thus we recommend against using it. If you have it already, you can get rid of it by<br>- uninstalling package `grub-customizer`<br>- removing folder tree `/etc/grub.d`<br>- reinstalling package `grub`<br>In case you have problems doing this, please come to the [forum](https://forum.endeavouros.com/t/faq-why-you-should-not-use-grub-customizer) for more advice. |  Removing grub-customizer | grub-customizer
2023.02.18 | The `nvidia-inst` app currently does not support installing legacy drivers.<br>See our [wiki](https://discovery.endeavouros.com/nvidia/new-nvidia-driver-installer-nvidia-inst) and [this post](https://forum.endeavouros.com/t/trouble-installing-nvidia) for more info. | Older Nvidia GPUs | Nvidia
2022.12.04 | On updating the system if you get this kind of error:<br>`error: failed to commit transaction (conflicting files)`<br>`<package-name>: <file-name> exists in filesystem`<br>then, after checking the file(s) *can* be overwritten, you can fix it with command<br>`sudo pacman -Syu --overwrite <filename>`<br>or if there are many similar errors,<br>`sudo pacman -Syu --overwrite '*'`<br>See `man pacman` and [the forum](https://forum.endeavouros.com/t/manual-intevention-needed-python-cairo-conflicting-files-during-update) for more info.
2022.10.18 | New Nvidia GPUs (30xx and 40xx) may need a workaround for boot issues, a kernel parameter `ibt=off`. More info [here](https://wiki.archlinux.org/title/NVIDIA#Installation). || Nvidia GPU 30xx and 40xx
2022.10.14 | Package `eos-hooks` 1.8-1 has been released to most mirrors, and the rest will have it soon. After update, please check your /etc/pacman.conf and report if there are any related issues.
2022.10.13 | Package `eos-hooks` will be updated to 1.8-1 at Friday 2022.10.14, around 8 p.m. or 20 o'clock (both CET time zone).<br>This update will move the `[endeavouros]` repository before the Arch repositories in file `/etc/pacman.conf`.<br>Please report any issues about this at the [EndeavourOS forum](https://forum.endeavouros.com).<br>See also news at 2022.09.23 below. |<b>Important!</b>| repository order change
2022.10.11 | Package `grub-tools` has been removed from the EndeavourOS repository. Mirrors should get the change within two days. || grub-tools removed
2022.10.08 | Package `grub-tools` will be removed very soon from the EndeavourOS repo. This is due to the grub update issue, see the 2022.08.27 news below.<br>It is recommended that users remove this package from their system as well since it *may* conflict with Arch best practices for grub.| | `grub-tools` removal
2022.09.23 | To prepare for potential future package issues, the `[endeavouros]` repository will be moved before the Arch repos in file `/etc/pacman.conf`.<br>This will occur when package `eos-hooks` is updated to version 1.8-1.<br><br>If you prefer not to allow this, write the following line into `/etc/pacman.conf`:<br><pre># EOS do not modify</pre>*before* the update, with no additional text on that line.<br><br>Note that the move will be made only once, and file<br>`/etc/eos-repo-before-arch-repos.once` is used as a "move lock".<br><br>A later update of `eos-hooks` (after a few months from now) will no more make this move. | **Important!** | repository order in pacman.conf
2022.09.14 | New ISO release: **Artemis nova** is [available](https://endeavouros.com/latest-release)!<br><br>Like always,<br>- New installs: please use the latest available ISO.<br>- Existing installs: no need to reinstall, regular updates will freshen the system. | | ISO
2022.08.27 | Update of package `grub` may make UEFI systems unbootable.<br><br>Fix: after update run `grub-install` *before* reboot.<br>If you have already rebooted, then run `grub-install` using the USB installer.<br><br>See forum threads [here](https://forum.endeavouros.com/t/the-latest-grub-package-update-needs-some-manual-intervention) and [here](https://forum.endeavouros.com/t/grub-2-2-06-r322-gd9b4638c5-1-wont-boot-and-goes-straight-to-the-bios-after-update). | <b>Important!</b> | grub issue, UEFI
2022.08.22 | A major EndeavourOS server migration is going on. It may take a few days, please be patient!
2022.08.19 | `eos-sendlog` program may fail with the default clbin.com service.<br>Workaround: see [this forum post](https://forum.endeavouros.com/t/eos-sendlog-certificate-issue) | | eos-sendlog, certificate
2022.08.08 | Today's ISO release: **Artemis neo** || ISO
2022.06.23 | New ISO, Artemis, has been released! || ISO
2022.05.30 | Budgie desktop users: we recommend using package<br> `budgie-control-center` instead of `gnome-control-center`.<br>See [this](https://forum.endeavouros.com/t/please-change-to-budgie-control-center-and-not-use-gnome-control-center-on-budgie-anymore/27616) for more info. | | Budgie desktop
2022.04.27 | In certain use cases, the latest ISO, Apollo, may not be able to finish<br>the install process.<br>Please look [here](https://forum.endeavouros.com/t/apollo-iso-bug-is-fixed-for-most-users-and-also-a-workaround-for-those-who-need-it/26503) for a solution. | <b>Important!</b> | ISO fix
2022.04.08 | With *offline* install in Apollo: if package `eos-quickstart` is not be installed, use terminal command<br>`yay -S eos-quickstart` to install it. || offline install
2022.04.06 | The next ISO, **Apollo**, enables, by default:<br>- a firewall on the ISO and on the installed system<br>- bluetooth on the ISO (for testing with your hardware) but not on the installed system (like before) | | firewall, bluetooth
2022.04.05 | How to fix updating system after offline install on Atlantis neo: see [this post](https://forum.endeavouros.com/t/issue-updating-system-after-xfce4-offline-install-atlantis-neo/25635). |  | offline install, Atlantis neo
2022.03.30 | Welcome's installer now has a button showing the page how to customize what to install. || customization
2022.01.31 | Btrfs on SSD: consider removing the `autodefrag` option from partitions with a btrfs filesystem<br>in file `/etc/fstab`.<br>It has been reported that 5.16 kernel has a btrfs related bug that can wear out an SSD rapidly.<br> [More info](https://forum.endeavouros.com/t/psa-linux-5-16-has-major-regression-in-btrfs-causing-extreme-io-load/23446) | <b>Important!</b> | ssd, btrfs, kernel
2021.09.21 | Added a link on this page to [Known issues](known_issues.md).
2021.09.16 | Some apps (e.g. the **Software News** button in `Welcome`) may fetch information from a specific internet site.<br>Users can now configure which of the supported sites will be used for fetching the data.<br>This can help when a particular site is (temporarily or permanently) unavailable.<br>More information: see file `/etc/eos-script-lib-yad.conf`, variable `EOS_FILESERVER_SITE`.
2021.09.15 | In file `/etc/default/grub` you can use variable `GRUB_DISABLE_OS_PROBER`.<br>This can be used for enabling `os-prober` usage again, but note the potential *security risk* involved.<br>More information: [Grub manual](https://www.gnu.org/software/grub/manual/grub/grub.html)
2021.09.09 | Nvidia GPU users: the `UpdateInTerminal` app includes a compatibility check<br>for Nvidia driver *and* kernel updates. It will warn users if a kernel would be updated<br>but the corresponding Nvidia driver would not.<br>Note that the `Welcome` app uses the `UpdateInTerminal` app for system updates. | Nvidia GPU | nvidia, gpu, kernel
2021.08.27 | EndeavourOS ISO 2021.08.27 is now released, [download it](https://endeavouros.com/latest-release/)! <br> Note that reinstalling is *not* required because EndeavourOS has a rolling release model.<br>However, we strongly recommend using the latest ISO in all *new* installs. | New ISO
2021.08.16 | The `eos-apps-info` app from package `eos-bash-shared` has been moved to a new package `eos-apps-info`.<br>If you already have installed a recent version of `eos-bash-shared`, then be sure to<br> update `eos-bash-shared` *before* installing `eos-apps-info`.
2021.06.12 | Installations made with the April-2021 ISO *after* the release of `pacman` version 6<br>may not have all new pacman features in file `/etc/pacman.conf`.<br>In particular this means `pacman` does not use some *optimizations*<br>(like `ParallelDownloads`) available in version 6, but they can be manually added.<br>Please see [this link](https://forum.endeavouros.com/t/fresh-install-6-10-21-pacman-conf-no-paralelldownloads) for more information.
2021.05.08 | A dependency of `eos-bash-shared` has been changed from `yad` to `yad-eos`.<br>Now pacman may inform about a conflict between them. User should simply accept the change.<br>This change makes `yad-eos` as the default yad provider.
2021.04.24 | The Personal Commands feature of Welcome has a new and easier to use API.<br>To see more info, start Welcome -> Tips tab -> Tutorial button -> New simpler API.
2021.04.17 | New EndeavourOS ISO has landed!<br>It has great new features, package updates, and old known issues have been solved.<br>[Go grab it!](https://endeavouros.com/latest-release)
2021.04.07 | Changed the patched `yad` package name to `yad-eos` to avoid further confusion.<br>To use the patched yad, install `yad-eos`:<br>`sudo pacman -Syu yad-eos`
2021.03.29 | The Welcome app has a new button **Yad (patched)** under the **Add More Apps** tab.<br>This button installs the patched EndeavourOS version of yad.<br>Note that the button is visible only if your current yad version is older than<br> the EndeavourOS version.<br>See also the 2021.03.18 news item below. | Outdated (2021.05.08).
2021.03.27 | IMPORTANT: in the EndeavourOS *installer* the **Update this app!** button<br>on the Welcome app should not be used for now as it will prevent installing<br>due to incompatible library versions.<br>The next ISO release will not have this issue. | Use 2021.04.17 ISO instead.
2021.03.18 | To workaround the `yad` bug of too high window (e.g. in `akm`), we have created<br> an EndeavourOS version of `yad`.<br>One way to use it instead of the upstream version is edit file `/etc/pacman.conf`<br>and move the `[endeavouros]` repository specification as the first repo.<br> See [this page](https://github.com/endeavouros-team/PKGBUILDS/tree/master/yad) for more details.<br>See also the 2021.03.29 news item above! | Outdated (2021.05.08).
2021.03.15 | First version of this page.
