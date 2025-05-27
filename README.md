# termux-alpine-rootfs
My alpine rootfs for termux proot-distro project
---
## I. what this project contain
- alpine rootfs that I customized for a better experience
## II. what's inside the image?
- preconfigured zsh with powerlevel10k theme
- openrc installed & softlevel enabled (for services managing)
- sudo alternative (doas) preinstalled and configured (which doesn't included in the proot-distro's official rootfs)
> info: I haven't create a password yet, so don't worry
## III. installation
1. install termux first, update it using `yes | pkg up`
2. install necessary packages:
```bash
yes | pkg i proot-distro
```
3. go to "release" section on this repo
4. install "alpinefull.tar.gz" file
5. return to Termux, type:
```bash
termux-setup-storage
```
6. hit enter, allow on next screen
7. paste this command:
```bash
cp ~/storage/downloads/alpinefull.tar.gz ~ && pd restore alpinefull.tar.gz && pd login alpine
```
