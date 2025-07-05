# Journal Entry 01 - RHEL Environment Setup 

**Date:** 2025-07-04
**Focus:** Preparing for RHCSA -Installing RHEL 10 and Initial Configuration


---

### What I Did:
- Reviewd how to access and download Red Hat Enterprise Linux 10 via the official Developer Portal (developers.redhat.com)
- Set up a new virtual machine in **Oracle VirtualBox** and installed RHEL 10 using the **Server with GUI** environment
- enabled the root account and created a local admin user during installation 
- After installation. the system booted into comand-line only (`multi-user.target`)
     - Resolved by isolating and setting `graphical.target` as the default boot target:
      ```bash 
      sudo systemctl isolate graphical.target
      sudo systemctl set-default graphical.target
      ```
- Verified that the GUI was not installed by default (due to selecting the wrong environment group)
     - Installed the GUI using :
     ``` bash
     sudo dnf groupinstall "Server with GUI" -y
     sudo reboot
     ```


---


### VirtualBox Guest Additions (Mouse//Display Fix)
- Mouse integration and window resizing weren't working initially 
- inserted the **Guest Additions CD** via the VirtualBox menu
- Mounted the CD and ran the installer using:
     ``` bash
     sudo dnf install gcc make perl kernel-devel kernel-headers elfutils-libelf-devel -y
     sudo mount /dev/cdrom /mnt
     sudo sh /mnt/VBoxLinuxAdditions.run
     sudo reboot
     ```
- Confirmed working mouse and dynamic screen resizing and after reboot


---


### GitHub SSH Setup and Journal Sync (RHEL virtual machine)
- Generated an SSH key on the RHEL system:
     ```bash
     ssh-keygen -t ed25519 -C "quemoy4u@gmail.com"
     ```
-Copied the public key and added it to GitHub under **Settings --> SSH and GPG Keys**
- Tested connection with:
    ``` bash
    ssh -T git@github.com
    ```
- Cloned existing GitHub journal repository into the RHEL VM:
     ``` bash
     git clone git@github.com:crawfan/it-learning-journal.git
     cd it-learning-journal
     ```


--- 


### Key Takeaways:
- Always verify your **Base Environment Group** during installation
