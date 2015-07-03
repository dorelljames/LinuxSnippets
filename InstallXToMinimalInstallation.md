Installing X to a Minimal Installation (RPM Way)
==================================================

On Fedora 19, install the following RPMs using YUM

```bash
Command: yum install package_name
Where: package_name is the name of the rpm (ex: xorg-x11-intel)

Example: yum install xorg-x11-intel
```

```bash
1.) yum -y install xterm xorg-x11-twm xorg-x11-drv-nouveau xorg-x11-drv-intel xorg-x11-drv-fbdev xorg-x11-drv-vesa xorg-x11-drv-evdev xorg-x11-drv-keyboard xorg-x11-drv-mouse xorg-x11-fonts-100dpi xorg-x11-server-Xorg xorg-x11-server-common xorg-x11-server-utils xorg-x11-xinit
```

EDIT: As of July 7, 2015 for Fedora 22 (Use dnf; yum is deprecated. xorg-x11-drv-keyboard & xorg-x11-drv-mouse removed)

```bash
1.) dnd -y install xterm xorg-x11-twm xorg-x11-drv-nouveau xorg-x11-drv-intel xorg-x11-drv-fbdev xorg-x11-drv-vesa xorg-x11-drv-evdev xorg-x11-fonts-100dpi xorg-x11-server-Xorg xorg-x11-server-common xorg-x11-server-utils xorg-x11-xinit
```

NOTE: Yum will query for dependencies of course.

# Additionals

```bash
2.) echo "exec twm" > ~/.xinitrc # Starts TWM when we startx
3.) yum -y install net-tools # Installs ifconfig and other related stuff
4.) yum -y install psmisc # Installs killall. Example usage: killall X
5.) yum -y install metacity # Installs metacity (window manager)
6.) yum -y install xterm # Installs xterm
```
