# EndeavourOS software news

[![Maintenance](https://img.shields.io/maintenance/yes/2022.svg)]()

[Download the latest ISO](https://endeavouros.com/latest-release)

[Known issues](known_issues.md)


Up to date news for the users the EndeavourOS software, like manual interventions, important code changes, and more.

Date | Description | Additional remarks | Tags
:--- | :--- | :---- | :---
2022-Aug-25 | Update of package `grub` may make UEFI systems unbootable.<br>Workaround: downgrade `grub` e.g. using the USB installer.<br>See the forum thread [here](https://forum.endeavouros.com/t/grub-2-2-06-r322-gd9b4638c5-1-wont-boot-and-goes-straight-to-the-bios-after-update). | | grub, downgrade
2022-Aug-22 | A major EndeavourOS server migration is going on. It may take a few days, please be patient!
2022-Aug-19 | `eos-sendlog` program may fail with the default clbin.com service.<br>Workaround: see [this forum post](https://forum.endeavouros.com/t/eos-sendlog-certificate-issue) | | eos-sendlog, certificate
2022-Aug-08 | Today's ISO release: **Artemis neo** || ISO
2022-Jun-23 | New ISO, Artemis, has been released! || ISO
2022-May-30 | Budgie desktop users: we recommend using package<br> `budgie-control-center` instead of `gnome-control-center`.<br>See [this](https://forum.endeavouros.com/t/please-change-to-budgie-control-center-and-not-use-gnome-control-center-on-budgie-anymore/27616) for more info. | | Budgie desktop
2022-Apr-27 | In certain use cases, the latest ISO, Apollo, may not be able to finish<br>the install process.<br>Please look [here](https://forum.endeavouros.com/t/apollo-iso-bug-is-fixed-for-most-users-and-also-a-workaround-for-those-who-need-it/26503) for a solution. | <b>Important!</b> | ISO fix
2022-Apr-08 | With *offline* install in Apollo: if package `eos-quickstart` is not be installed, use terminal command<br>`yay -S eos-quickstart` to install it. || offline install
2022-Apr-06 | The next ISO, **Apollo**, enables, by default:<br>- a firewall on the ISO and on the installed system<br>- bluetooth on the ISO (for testing with your hardware) but not on the installed system (like before) | | firewall, bluetooth
2022-Apr-05 | How to fix updating system after offline install on Atlantis neo: see [this post](https://forum.endeavouros.com/t/issue-updating-system-after-xfce4-offline-install-atlantis-neo/25635). |  | offline install, Atlantis neo
2022-Mar-30 | Welcome's installer now has a button showing the page how to customize what to install. || customization
2022-Jan-31 | Btrfs on SSD: consider removing the `autodefrag` option from partitions with a btrfs filesystem<br>in file `/etc/fstab`.<br>It has been reported that 5.16 kernel has a btrfs related bug that can wear out an SSD rapidly.<br> [More info](https://forum.endeavouros.com/t/psa-linux-5-16-has-major-regression-in-btrfs-causing-extreme-io-load/23446) | <b>Important!</b> | ssd, btrfs, kernel
2021-Sep-21 | Added a link on this page to [Known issues](known_issues.md).
2021-Sep-16 | Some apps (e.g. the **Software News** button in `Welcome`) may fetch information from a specific internet site.<br>Users can now configure which of the supported sites will be used for fetching the data.<br>This can help when a particular site is (temporarily or permanently) unavailable.<br>More information: see file `/etc/eos-script-lib-yad.conf`, variable `EOS_FILESERVER_SITE`.
2021-Sep-15 | In file `/etc/default/grub` you can use variable `GRUB_DISABLE_OS_PROBER`.<br>This can be used for enabling `os-prober` usage again, but note the potential *security risk* involved.<br>More information: [Grub manual](https://www.gnu.org/software/grub/manual/grub/grub.html)
2021-Sep-09 | Nvidia GPU users: the `UpdateInTerminal` app includes a compatibility check<br>for Nvidia driver *and* kernel updates. It will warn users if a kernel would be updated<br>but the corresponding Nvidia driver would not.<br>Note that the `Welcome` app uses the `UpdateInTerminal` app for system updates. | Nvidia GPU | nvidia, gpu, kernel
2021-Aug-27 | EndeavourOS ISO 2021-Aug-27 is now released, [download it](https://endeavouros.com/latest-release/)! <br> Note that reinstalling is *not* required because EndeavourOS has a rolling release model.<br>However, we strongly recommend using the latest ISO in all *new* installs. | New ISO
2021-Aug-16 | The `eos-apps-info` app from package `eos-bash-shared` has been moved to a new package `eos-apps-info`.<br>If you already have installed a recent version of `eos-bash-shared`, then be sure to<br> update `eos-bash-shared` *before* installing `eos-apps-info`.
2021-Jun-12 | Installations made with the April-2021 ISO *after* the release of `pacman` version 6<br>may not have all new pacman features in file `/etc/pacman.conf`.<br>In particular this means `pacman` does not use some *optimizations*<br>(like `ParallelDownloads`) available in version 6, but they can be manually added.<br>Please see [this link](https://forum.endeavouros.com/t/fresh-install-6-10-21-pacman-conf-no-paralelldownloads) for more information.
2021-May-08 | A dependency of `eos-bash-shared` has been changed from `yad` to `yad-eos`.<br>Now pacman may inform about a conflict between them. User should simply accept the change.<br>This change makes `yad-eos` as the default yad provider.
2021-Apr-24 | The Personal Commands feature of Welcome has a new and easier to use API.<br>To see more info, start Welcome -> Tips tab -> Tutorial button -> New simpler API.
2021-Apr-17 | New EndeavourOS ISO has landed!<br>It has great new features, package updates, and old known issues have been solved.<br>[Go grab it!](https://endeavouros.com/latest-release)
2021-Apr-07 | Changed the patched `yad` package name to `yad-eos` to avoid further confusion.<br>To use the patched yad, install `yad-eos`:<br>`sudo pacman -Syu yad-eos`
2021-Mar-29 | The Welcome app has a new button **Yad (patched)** under the **Add More Apps** tab.<br>This button installs the patched EndeavourOS version of yad.<br>Note that the button is visible only if your current yad version is older than<br> the EndeavourOS version.<br>See also the 2021-Mar-18 news item below. | Outdated (2021-May-08).
2021-Mar-27 | IMPORTANT: in the EndeavourOS *installer* the **Update this app!** button<br>on the Welcome app should not be used for now as it will prevent installing<br>due to incompatible library versions.<br>The next ISO release will not have this issue. | Use 2021-Apr-17 ISO instead.
2021-Mar-18 | To workaround the `yad` bug of too high window (e.g. in `akm`), we have created<br> an EndeavourOS version of `yad`.<br>One way to use it instead of the upstream version is edit file `/etc/pacman.conf`<br>and move the `[endeavouros]` repository specification as the first repo.<br> See [this page](https://github.com/endeavouros-team/PKGBUILDS/tree/master/yad) for more details.<br>See also the 2021-Mar-29 news item above! | Outdated (2021-May-08).
2021-Mar-15 | First version of this page.
