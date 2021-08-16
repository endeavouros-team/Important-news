# EndeavourOS software news
Up to date news for the users the EndeavourOS software, like manual interventions, important code changes, and more.

Date | Description | Additional remarks
:--- | :--- | :----
2021-Aug-16 | The `eos-apps-info` app from package `eos-bash-shared` has been moved to a new package `eos-apps-info`.<br>If you already have installed a recent version of `eos-bash-shared`, then be sure to update<br>`eos-bash-shared` *before* installing `eos-apps-info`.
2021-Jun-12 | Installations made with the April-2021 ISO *after* the release of `pacman` version 6<br>may not have all new pacman features in file `/etc/pacman.conf`.<br>In particular this means `pacman` does not use some *optimizations*<br>(like `ParallelDownloads`) available in version 6, but they can be manually added.<br>Please see [this link](https://forum.endeavouros.com/t/fresh-install-6-10-21-pacman-conf-no-paralelldownloads) for more information.
2021-May-08 | A dependency of `eos-bash-shared` has been changed from `yad` to `yad-eos`.<br>Now pacman may inform about a conflict between them. User should simply accept the change.<br>This change makes `yad-eos` as the default yad provider.
2021-Apr-24 | The Personal Commands feature of Welcome has a new and easier to use API.<br>To see more info, start Welcome -> Tips tab -> Tutorial button -> New simpler API.
2021-Apr-17 | New EndeavourOS ISO has landed!<br>It has great new features, package updates, and old known issues have been solved.<br>[Go grab it!](https://endeavouros.com/latest-release)
2021-Apr-07 | Changed the patched `yad` package name to `yad-eos` to avoid further confusion.<br>To use the patched yad, install `yad-eos`:<br>`sudo pacman -Syu yad-eos`
2021-Mar-29 | The Welcome app has a new button **Yad (patched)** under the **Add More Apps** tab.<br>This button installs the patched EndeavourOS version of yad.<br>Note that the button is visible only if your current yad version is older than<br> the EndeavourOS version.<br>See also the 2021-Mar-18 news item below. | Outdated (2021-May-08).
2021-Mar-27 | IMPORTANT: in the EndeavourOS *installer* the **Update this app!** button<br>on the Welcome app should not be used for now as it will prevent installing<br>due to incompatible library versions.<br>The next ISO release will not have this issue. | Use 2021-Apr-17 ISO instead.
2021-Mar-18 | To workaround the `yad` bug of too high window (e.g. in `akm`), we have created<br> an EndeavourOS version of `yad`.<br>One way to use it instead of the upstream version is edit file `/etc/pacman.conf`<br>and move the `[endeavouros]` repository specification as the first repo.<br> See [this page](https://github.com/endeavouros-team/PKGBUILDS/tree/master/yad) for more details.<br>See also the 2021-Mar-29 news item above! | Outdated (2021-May-08).
2021-Mar-15 | First version of this page.
