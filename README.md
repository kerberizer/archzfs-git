# archzfs-git

These are [Arch](https://www.archlinux.org/) Linux [PKGBUILDs](https://wiki.archlinux.org/index.php/PKGBUILD) for [ZFS on Linux](http://zfsonlinux.org/) (ZoL) based on the [master branch](https://github.com/zfsonlinux/zfs).

The PKGBUILDs were started as a fork of the wonderful work done by [@demizer](https://github.com/demizer) to be tailored for my own needs. They have thus since diverged in some ways from the original. Feel free to use them if you like—I tend to update them pretty often—but please also understand that, unfortunately, **I cannot offer any support for them**. Unless you really know what you're doing, I strongly suggest that you instead use the semi-official packages at [archzfs/archzfs](https://github.com/archzfs/archzfs).

**Important notice:** ZFS will fail to load properly the pools and datasets without the right systemd units enabled. A [preset](https://www.freedesktop.org/software/systemd/man/systemd.preset.html) file with sane defaults is included. It can be easily applied by e.g. running the following command:

``` shell-script
systemctl preset \
    $(tail -n +2 /usr/lib/systemd/system-preset/50-zfs.preset | cut -d ' ' -f 2)
```
**Notice:** You'll need a recent version of [GRUB](https://www.gnu.org/software/grub/) to be able to boot from a ZFS pool, especially from one that has more feature flags enabled. The official [GRUB package](https://www.archlinux.org/packages/core/x86_64/grub/) from Arch's core repo should in most cases work fine. Alternatively, the [grub-git](https://aur.archlinux.org/packages/grub-git/) package from AUR may be needed instead. The `grub-zfs` package that was included previously has been discontinued, as it got badly outdated and wasn't really needed any more, and is replaced in the repo by `grub-git`.

There is a publicly available [repository](http://kerberia.net/archlinux/repo/archzfs-git) with prebuilt, binary packages for both the `i686` and `x86_64` architectures, but these packages are also provided **as is**. In particular, the `i686` packages are not being tested at all and may even be dropped altogether at some point. The current package versions in the repo are as follows:
* `grub-git-2.02.beta3.22.ge563928-1`
* `spl-git-0.7.0.rc2.r0.g7b25c48_4.8.4r1-1`
* `spl-utils-git-0.7.0.rc2.r0.g7b25c48_4.8.4r1-1`
* `zfs-git-0.7.0.rc2.r0.gc6a89b5_4.8.4r1-1`
* `zfs-utils-git-0.7.0.rc2.r0.gc6a89b5_4.8.4r1-1`
