!SLIDE subsec

# Installing the Hypervisor

!SLIDE bullets rvc

# Hypervisor requirements

### **Mandatory** on all nodes

* _Xen_ 3.0 and above
* _KVM_ 72 or 0.11 and above
* Install via your distro
* Reboot as necessary

!SLIDE commandline bullets medcode

# Selecting the instance kernel

    $ cd /boot
    $ ln -s vmlinuz-2.6.32-32-server vmlinuz-2.6-xenU
    $ ln -s initrd.img-2.6.32-32-server initrd-2.6-xenU

* Create _symlink_ for instance
* _initrd_ not required 
