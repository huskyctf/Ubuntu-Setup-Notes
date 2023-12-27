# Ubuntu-Setup-Notes
Personal playbook for setting up or installing software on a fresh Ubuntu virtual machine (VM). Using Virtual Box as hypervisor and the standard Ubuntu desktop install. This is just my personal preference to get started, your requirements may differ so follow at your own risk.

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
sudo apt install build-essential dkms
```
Then on VirtualBox go to "Devices > Insert Guest Additions CD Image". Run the installation script as follows:

```bash
sudo /media/<user>/VBox_GAs_7.0.12/VBoxLinuxAdditions.run
```
Once installed unmount the disk by "Devices > Optical Drives > Remove Disk From Virtual Drive..."

## Enable dark mode and disable screen timeout 

```bash
gsettings set org.gnome.desktop.interface gtk-theme 'Yaru-dark'
```
```bash
gsettings set org.gnome.desktop.session idle-delay 0
```

## Media and audio playback

```bash
sudo apt install ffmpeg
```
Now shutdown the VM and go to the machine settings in Virtual Box. Navigate to "Audio > Audio Controller" and change it to "Intel HD Audio". Start the VM again.

## Install favourite packages and snaps

```bash
sudo snap install code --classic && sudo snap install sublime-text --classic
```
```bash
sudo apt install git flameshot vim cherrytree
```
Update the favourite pinned apps:
```bash
gsettings set org.gnome.shell favorite-apps "['firefox_firefox.desktop', 'org.gnome.Nautilus.desktop', 'code_code.desktop', 'cherrytree.desktop', 'org.flameshot.Flameshot.desktop', 'sublime-text_subl.desktop']"
```
