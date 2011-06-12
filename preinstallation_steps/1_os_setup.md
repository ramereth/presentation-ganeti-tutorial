!SLIDE bullets list

# Operating System Setup

* At least _20GB_ system volume
* _Single_ LVM Volume Group for instances
* 64bit is preferred

!SLIDE codeblock bigcode

# Typical Partition Layout

    /dev/sda1   /boot   200M
    /dev/sda2   /       10-20G
    /dev/sda3   LVM     rest, named ganeti

!SLIDE bullets

# Hostname Issues

* Requires _hostname_ to be the **FQDN**
* i.e. _node1.example.com_ instead of _node1_
