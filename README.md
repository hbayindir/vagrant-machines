# vagrant-machines
Contains commonly used Vagrant machine definitions to easily create VMs ready for development.

Otherwise noted, all VMs download the latest Virtualbox Guest additions image, has virtual networking IPs, run on VirtIO network cards and updates themselves to latest version of the OS automatically.

Currently contains the following VMs
- **debian-installer-development:** Debian Jessie 64bit which checkouts Debian Installer source repository, installs build dependencies and updates itself.
- **debian-xfce-development:** Debian Jessie 64bit which updates itself and installs `task-xfce-desktop` metapackage. Suited for working on XFCE desktop components or as a general purpose VM.
- **debian-lightdm-development:** Debian Jessie 64bit which updates itself and installs `task-xfce-desktop` metapackage. Also installs build dependencies of `lightdm` and downloads its latest source deb for lightdm development.
- **debian-selinux-development:** Debian Jessie 64bit which updates itself and installs a permissive SELinux environment with reference policy from Debian Unstable.
