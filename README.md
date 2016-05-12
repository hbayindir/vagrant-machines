# vagrant-machines
Contains commonly used Vagrant machine definitions to easily create VMs ready for development.

Otherwise noted, all VMs download the latest Virtualbox Guest additions image, has virtual networking IPs, run on VirtIO network cards and updates themselves to latest version of the OS automatically.

Currently contains the following VMs
- **debian-xfce-development:** Debian Jessie 64bit which updates itself and installs `task-xfce-desktop` metapackage. Suited for working on XFCE desktop components or as a general purpose VM.
- **debian-installer-development:** Debian Jessie 64bit which checkouts Debian Installer source repository, installs build dependencies and updates itself.
- **debian-lightdm-development:** Debian Jessie 64bit which updates itself and installs `task-xfce-desktop` metapackage. Also installs build dependencies of `lightdm` and downloads its latest source deb for lightdm development.
- **debian-selinux-development:** Debian Jessie 64bit which updates itself and installs a permissive SELinux environment with reference policy from Debian Unstable. Also downloads MLS policy, policy documentation, development packages and reference policy source.
- **debian-ldap-development:** Debian Jessie 64bit which updates itself and installs `slapd` (OpenLDAP server) and `ldap-utils` package. Designed to assist in development of LDAP schemas and related things. Redirects port 389 to 38983 on host. You need to run `dpkg-reconfigure slapd` once to configure your LDAP server after provisioning to set its specifics.
- **debian-squid-server:** Debian Jessie 64bit which updates itself and installs an unconfigured `squid3` server.

## Private IP List
Following list contains the Private IP addresses of the host-only networking interfaces of the machines.
- **debian-xfce-development:** `192.168.56.97`
- **debian-installer-development:** `192.168.56.96`
- **debian-lightdm-development:** `192.168.56.95`
- **debian-selinux-development:** `192.168.56.94`
- **debian-ldap-development:** `192.168.56.93`
- **debian-squid-server:** `192.168.56.92`
