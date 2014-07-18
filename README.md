These are Arch Linux PKGBUILDs for ZFS on Linux (ZoL) based on the Git master branch. They are based on the wonderful work done by [@demizer](https://github.com/demizer) at [demizer/archzfs](https://github.com/demizer/archzfs). The PKGBUILDs are here for information purposes and are **not** supposed to be used on production systems unless you really know what you are doing.

**Important notice:** For the ZFS datasets to be mounted and shared properly, it is imperative to enable `zfs.target` in systemd. Any old `zfs.service` should be disabled accordingly.

There is also a publicly available [repository](http://kerberia.net/archlinux/repo/archzfs-git) with packages for both the `i686` and `x86_64` architectures, but these packages are also provided *as is*, and the `i686` ones in particular have not been tested at all. The current package versions in the repo are as follows:
* spl-modules-git-0.6.3.r1.gf6a8696_3.15.5r2-1
* spl-utils-git-0.6.3.r1.gf6a8696_3.15.5r2-1
* zfs-modules-git-0.6.3.r14.g1e8db77_3.15.5r2-1
* zfs-utils-git-0.6.3.r14.g1e8db77_3.15.5r2-1
