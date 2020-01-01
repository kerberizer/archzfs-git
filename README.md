# archzfs-git

These are [Arch](https://www.archlinux.org/) Linux [PKGBUILDs](https://wiki.archlinux.org/index.php/PKGBUILD) for [ZFS on Linux](http://zfsonlinux.org/) (ZoL) based on the [master branch](https://github.com/zfsonlinux/zfs).

The PKGBUILDs were started as a fork of the wonderful work done by [@demizer](https://github.com/demizer) to be tailored for my own needs. They have thus since diverged in some ways from the original. Feel free to use them if you like—I tend to update them pretty often—but please also understand that, unfortunately, **I cannot offer any support for them**. Unless you really know what you're doing, I strongly suggest that you instead use the semi-official packages at [archzfs/archzfs](https://github.com/archzfs/archzfs).

**Important notice:** ZFS will fail to load properly the pools and datasets without the right systemd units enabled. A [preset](https://www.freedesktop.org/software/systemd/man/systemd.preset.html) file with sane defaults is included. It can be easily applied by e.g. running the following command:

``` shell-script
systemctl preset \
    $(tail -n +2 /usr/lib/systemd/system-preset/50-zfs.preset | cut -d ' ' -f 2)
```
**Notice:** You'll need a recent version of [GRUB](https://www.gnu.org/software/grub/) to be able to boot from a ZFS pool, especially from one that has more feature flags enabled. The official [GRUB package](https://www.archlinux.org/packages/core/x86_64/grub/) from Arch's core repo should in most cases work fine. Alternatively, the [grub-git](https://aur.archlinux.org/packages/grub-git/) package from AUR may be needed instead. The `grub-zfs` package that was included previously has been discontinued, as it got badly outdated and wasn't really needed any more, and is replaced in the repo by `grub-git`.

There is a publicly available [repository](https://repos.uni-plovdiv.net/archlinux/archzfs-git) with binary packages for the `x86_64` architecture, but it is also provided **as is**. The current package versions in the repo are as follows:
* `grub-git-2.04.r29.g0f3f5b7c1-1`
* `zfs-utils-git-0.8.0.r495.g82e996c26_5.4.7.arch1.r1-1`
* `zfs-git-0.8.0.r495.g82e996c26_5.4.7.arch1.r1-1`
