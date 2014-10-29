These are Arch Linux PKGBUILDs for ZFS on Linux (ZoL) based on the Git master branch. They are based on the wonderful work done by [@demizer](https://github.com/demizer) at [demizer/archzfs](https://github.com/demizer/archzfs). The PKGBUILDs are here for information purposes and are **not** supposed to be used on production systems unless you really know what you are doing.

**Important notice:** For the ZFS datasets to be mounted and shared properly, it is imperative to enable `zfs.target` in systemd. Any old `zfs.service` should be disabled accordingly.

There is also a publicly available [repository](http://kerberia.net/archlinux/repo/archzfs-git) with packages for both the `i686` and `x86_64` architectures, but these packages are also provided *as is*, and the `i686` ones in particular have not been tested at all. The current package versions in the repo are as follows:

* spl-modules-git-0.6.3.r48.g3f4a13c_3.17.1r1-1
* spl-utils-git-0.6.3.r48.g3f4a13c_3.17.1r1-1
* zfs-modules-git-0.6.3.r139.gbb9d808_3.17.1r1-1
