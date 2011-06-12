!SLIDE bullets

# Installing DRBD

* Required for _high availability_
* Can _upgrade_ to DRBD later
* Need at least _8.0.12_
* Distro Support

!SLIDE codeblock rvc

# DRBD Module Setup

### Via modules

    $ echo drbd minor_count=255 usermode_helper=/bin/true >> /etc/modules
    $ depmod -a
    $ modprobe drbd minor_count=255 usermode_helper=/bin/true

### Via Grub

    # Kernel Commands
    drbd.minor_count=255 drbd.usermode_helper=/bin/true
