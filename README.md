These are Arch Linux PKGBUILDs for ZFS on Linux (ZoL) based on the Git master branch. They are based on the wonderful work done by [@demizer](https://github.com/demizer) at [demizer/archzfs](https://github.com/demizer/archzfs). The PKGBUILDs are here for information purposes and are **not** supposed to be used on production systems unless you really know what you are doing.

**Important notice:** For the ZFS datasets to be mounted and shared properly, it is imperative to enable `zfs.target` in systemd. Any old `zfs.service` should be disabled accordingly.
* spl-modules-git-0.6.3.r50.g917fef2_3.17.3r1-1
* spl-utils-git-0.6.3.r50.g917fef2_3.17.3r1-1
* zfs-modules-git-0.6.3.r155.g7b2d78a_3.17.3r1-1
* zfs-utils-git-0.6.3.r155.g7b2d78a_3.17.3r1-1
