!SLIDE bullets

# Installing DRBD

* Required for high availability
* Can upgrade to DRBD later
* Need at least 8.0.12
* Distro Support

!SLIDE codeblock

# DRBD Module Setup

## Via modules

    $ echo drbd minor_count=255 usermode_helper=/bin/true >> /etc/modules
    $ depmod -a
    $ modprobe drbd minor_count=255 usermode_helper=/bin/true

## Via Grub

    # Kernel Commands
    drbd.minor_count=255 drbd.usermode_helper=/bin/true
