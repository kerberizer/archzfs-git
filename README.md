These are Arch Linux PKGBUILDs for ZFS on Linux (ZoL) based on the Git master branch. They are based on the wonderful work done by [@demizer](https://github.com/demizer) at [demizer/archzfs](https://github.com/demizer/archzfs). The PKGBUILDs are here for information purposes and are **not** supposed to be used on production systems unless you really know what you are doing.

**Important notice:** For the ZFS datasets to be mounted and shared properly, it is imperative to enable `zfs.target` in systemd. Any old `zfs.service` should be disabled accordingly.

Since the support in [GRUB](https://www.gnu.org/software/grub/) for ZFS tends to lag behind ZoL development, a separate `grub-zfs` package is provided with support for the latest ZFS pool feature flags. With the the standard [GRUB package](https://www.archlinux.org/packages/core/x86_64/grub/) from Arch's core repo the system boots, but grub-install cannot recognize the ZFS pool devices as such. Many thanks to [@dweeezil](https://github.com/dweeezil) for having published the needed patches [here on GitHub](https://github.com/dweeezil/grub/commits/zfs).

There is also a publicly available [repository](http://kerberia.net/archlinux/repo/archzfs-git) with packages for both the `i686` and `x86_64` architectures, but these packages are also provided *as is*, and the `i686` ones in particular have not been tested at all. The current package versions in the repo are as follows:
* `grub-zfs-2.02.beta2-1`
* `spl-git-0.6.3.r76.g6ab0866_3.19.2r1-1`
* `spl-utils-git-0.6.3.r76.g6ab0866_3.19.2r1-1`
* `zfs-git-0.6.3.r242.g5c3f61e_3.19.2r1-1`
* `zfs-utils-git-0.6.3.r242.g5c3f61e_3.19.2r1-1`
