# pkgbuilds

This is a collection of the `PKGBUILD` files (Arch User Repository install files) that I maintain.

Feel free to submit PRs if you want to see a change or an update, I'll be likely to merge, test, and push soon.

 - [python313](python313/)
   [![AUR](https://img.shields.io/aur/votes/python313.svg)](https://aur.archlinux.org/packages/python313)
 - [python312](python312/)
 - [python39](python39/)
   [![AUR](https://img.shields.io/aur/votes/python39.svg)](https://aur.archlinux.org/packages/python39)
 - [python38](python38/)
   [![AUR](https://img.shields.io/aur/votes/python38.svg)](https://aur.archlinux.org/packages/python38)
 - [python36](python36/)
   [![AUR](https://img.shields.io/aur/votes/python36.svg)](https://aur.archlinux.org/packages/python36)
 - [hostmux](hostmux-git/)
   [![AUR](https://img.shields.io/aur/votes/hostmux-git.svg)](https://aur.archlinux.org/packages/hostmux-git)
 - [augenkrebs](augenkrebs-git/)
   [![AUR](https://img.shields.io/aur/votes/augenkrebs-git.svg)](https://aur.archlinux.org/packages/augenkrebs-git)

## Discontinued pkgbuilds

Archived pkgbuilds can be found in ``archived``, which includes

 - ``python35`` removed due to age

## Python package FAQ

I'm mostly putting these here so I have a way to copy and paste a friendly answer for questions on aur.archlinux.org.

### y u no optimizations??

This package intentionally doesn't use ``--enable-optimizations``. Enabling optimizations adds a lot of build time – I
for one would not upgrade my Python as regularly if every update took 25-40 minutes of heavy CPU use (depending on your
machine, but laptop was pretty beefy when I got it three years ago, and even 3.11 takes 25 minutes on it). Adding the
flag is easy to do on your own – grab the repo, add the flag, ``makepkg``. Imo adding it by default would be a poor
choice.

### pls add provides=Python

Nope. Been there, done that, got chewed out for it. tl;dr: Provides=Python makes the system assume that if you have
Python from core and Python from AUR installed, and you remove core Python, then all Python dependencies will continue
working. Which they won't, obv, so adding `provides=(Python)` (yes, even with a version string!) is misleading and bad.

## Usage for maintainers

These instructions are just intended for me, rixx – you don't have to run through these steps when you submit a PR!

1. In sub-directory: Edit `PKGBUILD`
2. `makepkg --check`
3. `namcap PKGBUILD`
4. `namcap *.zst`
5. `makepkg --printsrcinfo > .SRCINFO`
6. `git commit -am 'Meaningful commit message'`
7. `git push`
8. In root directory: `git commit -am [package] Meaningful commit message`


## Resources

 - [general AUR article](https://wiki.archlinux.org/index.php/Arch_User_Repository)
 - [Creating packages](https://wiki.archlinux.org/index.php/Creating_packages)
 - [Arch packaging standards](https://wiki.archlinux.org/index.php/Arch_packaging_standards)
 - [PKGBUILD](https://wiki.archlinux.org/index.php/PKGBUILD)
 - [makepkg](https://wiki.archlinux.org/index.php/Makepkg)
 - [.SRCINFO](https://wiki.archlinux.org/index.php/.SRCINFO)
 - [VCS package guidelines](https://wiki.archlinux.org/index.php/VCS_package_guidelines)
 - [Namcap](https://wiki.archlinux.org/index.php/Namcap)
