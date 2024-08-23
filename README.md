# Ubuntu-Setup-Notes
Personal playbook for setting up or installing software on a fresh Ubuntu virtual machine (VM). Using Virtual Box as hypervisor and the minimal 22.04 Ubuntu desktop install with additional drivers. This is just my personal preference to get started, your requirements may differ so follow at your own risk.

## Update all packages and snaps

```bash
sudo apt update && sudo apt full-upgrade
```
```bash
sudo snap refresh
```

## Enable firewall

```bash
sudo ufw enable
```

## Installing Virtual Box Guest Additions

```bash
sudo apt install virtualbox-guest-additions-iso
```
Navigate to the location `/usr/share/virtualbox/VBoxGuestAdditions.iso` and right click "mount" the image. Then run:

```bash
sudo ./VBoxLinuxAdditions.run
```
Once installed unmount the disk again by right clicking and selecting "unmount". Reboot the machine for the update to take effect.

## Enable dark mode and disable screen timeout 

```bash
gsettings set org.gnome.desktop.interface gtk-theme 'Yaru-dark'
```
```bash
gsettings set org.gnome.desktop.session idle-delay 0
```

## Install favourite packages and snaps

```bash
sudo apt install git flameshot vim cherrytree ffmpeg ghostwriter
```
Update the favourite pinned apps:
```bash
gsettings set org.gnome.shell favorite-apps "['firefox_firefox.desktop', 'org.gnome.Nautilus.desktop', 'cherrytree.desktop', 'org.flameshot.Flameshot.desktop']"
```

## Set a desktop wallpaper (optional)

User dwt1 on gitlab has a collection of [wallpapers](https://gitlab.com/dwt1/wallpapers) that may be of interest.
