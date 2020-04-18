# vagrant-machines
Contains commonly used Vagrant machine definitions to easily create VMs ready for development.

Otherwise noted, all VMs have virtual networking IPs, run on VirtIO network cards and updates themselves to latest version of the OS automatically. For automatic installation of VirtualBox guest additions, please use `vagrant-vbguest` plugin.

Currently contains the following VMs
- **debian-xfce-development:** Debian Jessie 64bit which updates itself and installs `task-xfce-desktop` metapackage. Suited for working on XFCE desktop components or as a general purpose VM.
- **debian-installer-development:** Debian Jessie 64bit which checkouts Debian Installer source repository, installs build dependencies and updates itself.
- **debian-lightdm-development:** Debian Jessie 64bit which updates itself and installs `task-xfce-desktop` metapackage. Also installs build dependencies of `lightdm` and downloads its latest source deb for lightdm development.
- **debian-selinux-development:** Debian Jessie 64bit which updates itself and installs a permissive SELinux environment with reference policy from Debian Unstable. Also downloads MLS policy, policy documentation, development packages and reference policy source.
- **debian-ldap-development:** Debian Jessie 64bit which updates itself and installs `slapd` (OpenLDAP server) and `ldap-utils` package. Designed to assist in development of LDAP schemas and related things. Redirects port 389 to 38983 on host. You need to run `dpkg-reconfigure slapd` once to configure your LDAP server after provisioning to set its specifics.
- **debian-squid-server:** Debian Jessie 64bit which updates itself and installs an unconfigured `squid3` server.
- **debian-docker-lab:** Debian Stretch 64bit which updates itself and installs latest [docker](https://www.docker.com/) from official repositories. RAM is set to 2536MB (2.5GB) to make sure it can run some containers.
- **debian-custom-image-builder:** Debian Jessie 64bit which updates itself and installs packages and tools required to create custom debian installation media (both classic and live variants). Live image building tools are taken from Stretch.
- **debian-grive-builder:** Debian Stretch 64bit which updates itself and installs packages and tools required to build [grive](https://github.com/Grive/grive) Google Drive client. After the machine is up, the client can be directly built (see the post-up message).
- **centos7-kubernetes-cluster:** A pair of CentOS 7 64bit VMs which update themselves, install [docker](https://www.docker.com) and [kubernetes](https://kubernetes.io). The cluster is only installed, but not configured (Please see the post-up message).
- **centos7-rpm-builder:** A CentOS 7 minimal system which installs and sets up an environment for building `RPM` files from scratch.
- **debian-covid19-dashboard-development:** Debian Buster 64bit which updates itself and installs the required environment plus `webfs` to develop and test [Turkey COVID-19 statistics dashboard](https://github.com/hbayindir/covid-19-turkey). This VM also copies your `~/.gitconfig` to `~` to make development easier.

## Private IP List
Following list contains the Private IP addresses of the host-only networking interfaces of the machines.
- **debian-xfce-development:** `192.168.56.97`
- **debian-installer-development:** `192.168.56.96`
- **debian-lightdm-development:** `192.168.56.95`
- **debian-selinux-development:** `192.168.56.94`
- **debian-ldap-development:** `192.168.56.93`
- **debian-squid-server:** `192.168.56.92`
- **debian-docker-lab:** `192.168.56.91`
- **debian-custom-image-builder:** `192.168.56.90`
- **debian-grive-builder:** `192.168.56.89`
- **centos7-kubernetes-cluster:**
  - **`master`:** `192.168.56.87`
  - **`node-1`:** `192.168.56.86`
- **centos7-rpm-builder:** `192.168.56.85`
- **debian-covid19-dashboard-development:** `192.168.56.84`
