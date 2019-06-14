# IPFS-Cluster workshops

This repository contains documents and setup related to IPFS-Cluster workshops


## Raspberry PI pre-requirements

* Enable ssh by default by placing an `ssh` in the root of the boot partition
* Add SSH key to authorized keys for pi and root users
* Install emacs-nox, jq
* Disable password login
* raspi-config to set hostname, enable serial comms, enable sshd, expand filesystem
* rpi-update to update firmware
* Reboot and run ansible like `ansible-playbook -i inventory.yml workshop.yml -u root`
