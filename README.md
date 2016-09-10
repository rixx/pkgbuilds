# pkgbuilds

This is a collection of the `PKGBUILD` files (Arch User Repository install files) that I maintain.

## Usage

1. Edit `PKGBUILD`
2. `makepkg --check`
3. `namcap PKGBUILD`
4. `namcap *.xz`
5. `makepkg --printsrcinfo > .SRCINFO`
6. `git commit -am 'Meaningful commit message'`
7. `git push`


## Index

### in AUR

 - [augenkrebs](augenkrebs-git/)
 - [hostmux](hostmux-git/)
 - [python36](python36/)

### private


## Resources

 - [general AUR article](https://wiki.archlinux.org/index.php/Arch_User_Repository)
 - [Creating packages](https://wiki.archlinux.org/index.php/Creating_packages)
 - [Arch packaging standards](https://wiki.archlinux.org/index.php/Arch_packaging_standards)
 - [PKGBUILD](https://wiki.archlinux.org/index.php/PKGBUILD)
 - [makepkg](https://wiki.archlinux.org/index.php/Makepkg)
 - [.SRCINFO](https://wiki.archlinux.org/index.php/.SRCINFO)
 - [VCS package guidelines](https://wiki.archlinux.org/index.php/VCS_package_guidelines)
 - [Namcap](https://wiki.archlinux.org/index.php/Namcap)

## Structure

I decided to avoid the clusterfuck that is submodules (on a maybe-stable remote, with its own magic hooks everywhere),
but in truth, every subfolder of this repo is a repo on my machine. Since only I as maintainer can push to those repos
anyway, I think we should be fine here.
