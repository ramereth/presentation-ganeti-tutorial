!SLIDE bullets list

# Operating System Setup

* Clean ,minimal system install
* Minimum _20GB_ system volume
* _Single_ LVM Volume Group for instances
* 64bit is preferred
* _Similar_ hardware/software configuration across nodes

!SLIDE codeblock bigcode

# Partition Layout

    /dev/sda1   /boot   200M
    /dev/sda2   /       10-20G
    /dev/sda3   LVM     rest, named ganeti

!SLIDE bullets list redcode

# Hostname Issues

* Requires _hostname_ to be the **FQDN**
* i.e. _node1.example.com_ instead of _node1_
* `hostname --fqdn` requires resolver library
* Reduce dependency on DNS and _guessing_
