# archzfs-git

These are [Arch](https://www.archlinux.org/) Linux [PKGBUILDs](https://wiki.archlinux.org/index.php/PKGBUILD) for [ZFS on Linux](http://zfsonlinux.org/) (ZoL) based on the [master branch](https://github.com/zfsonlinux/zfs).

The PKGBUILDs were started as a fork of the wonderful work done by [@demizer](https://github.com/demizer) to be tailored for my own needs. They have thus since diverged in some ways from the original. Feel free to use them if you like—I tend to update them pretty often—but please also understand that, unfortunately, **I cannot offer any support for them**. Unless you really know what you're doing, I strongly suggest that you instead use the semi-official packages at [archzfs/archzfs](https://github.com/archzfs/archzfs).

**Important notice:** ZFS will fail to load properly the pools and datasets without the right systemd units enabled. A [preset](https://www.freedesktop.org/software/systemd/man/systemd.preset.html) file with sane defaults is included. It can be easily applied by e.g. running the following command:

* `spl-git-0.7.0.r13.ge8474f9_4.13.4r1-1`
* `spl-utils-git-0.7.0.r13.ge8474f9_4.13.4r1-1`
* `zfs-git-0.7.0.r103.ga0430cc5a_4.13.4r1-1`
* `zfs-utils-git-0.7.0.r103.ga0430cc5a_4.13.4r1-1`
