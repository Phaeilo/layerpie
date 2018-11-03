# layerpie
This repository contains some utilities to configure Raspbian with an OverlayFS root file system.
The SD card will be mounted read-only and all writes will be redirected to a tmpfs in RAM.
This will provide a robust file-system configuration and reduce the possibility of corruption.

## Download & Install

Go to the "release" section of this repository and download the latest installer script.
Next, run it as root on Raspbian: `sudo sh installer`

Alternatively, you can also get the installer by cloning this GIT repository:
```
git clone https://github.com/Phaeilo/layerpie.git
cd layerpie
sh mk_installer
sudo sh installer
```

## Usage

Use the `lpie` command to configure the OverlayFS state:

 * `lpie status` displays the current state
 * `sudo lpie enable` enables OverlayFS on next boot
 * `sudo lpie disable` disables OverlayFS on next boot
 * `sudo lpie reboot-rw` reboots the system without OverlayFS once

