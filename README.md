# pkgbuilds

This is a collection of the `PKGBUILD` files (Arch User Repository install files) that I maintain.

Feel free to submit PRs if you want to see a change or an update, I'll be likely to merge, test, and push soon.

 - [python311](python311/)
   [![AUR](https://img.shields.io/aur/votes/python311.svg)](https://aur.archlinux.org/packages/python311)
 - [python310](python310/)
   [![AUR](https://img.shields.io/aur/votes/python310.svg)](https://aur.archlinux.org/packages/python310)
 - [python39](python39/)
   [![AUR](https://img.shields.io/aur/votes/python39.svg)](https://aur.archlinux.org/packages/python39)
 - [python38](python38/)
   [![AUR](https://img.shields.io/aur/votes/python38.svg)](https://aur.archlinux.org/packages/python38)
 - [python36](python36/)
   [![AUR](https://img.shields.io/aur/votes/python36.svg)](https://aur.archlinux.org/packages/python36)
 - [python35](python35/)
   [![AUR](https://img.shields.io/aur/votes/python35.svg)](https://aur.archlinux.org/packages/python35)
 - [hostmux](hostmux-git/)
   [![AUR](https://img.shields.io/aur/votes/hostmux-git.svg)](https://aur.archlinux.org/packages/hostmux-git)
 - [augenkrebs](augenkrebs-git/)
   [![AUR](https://img.shields.io/aur/votes/augenkrebs-git.svg)](https://aur.archlinux.org/packages/augenkrebs-git)

## Usage

1. Edit `PKGBUILD`
2. `makepkg --check`
3. `namcap PKGBUILD`
4. `namcap *.xz`
5. `makepkg --printsrcinfo > .SRCINFO`
6. `git commit -am 'Meaningful commit message'`
7. `git push`


## Resources

 - [general AUR article](https://wiki.archlinux.org/index.php/Arch_User_Repository)
 - [Creating packages](https://wiki.archlinux.org/index.php/Creating_packages)
 - [Arch packaging standards](https://wiki.archlinux.org/index.php/Arch_packaging_standards)
 - [PKGBUILD](https://wiki.archlinux.org/index.php/PKGBUILD)
 - [makepkg](https://wiki.archlinux.org/index.php/Makepkg)
 - [.SRCINFO](https://wiki.archlinux.org/index.php/.SRCINFO)
 - [VCS package guidelines](https://wiki.archlinux.org/index.php/VCS_package_guidelines)
 - [Namcap](https://wiki.archlinux.org/index.php/Namcap)
