!SLIDE commandline incremental medcode

# Accessing an instance's disks

    $ gnt-instance activate-disks INSTANCE
    $ gnt-instance activate-disks instance1
    $ ssh node3
    kpartx -l /dev/…
    kpartx -a /dev/…
    mount /dev/mapper/… /mnt/
    $ # edit files under mnt as desired
    umount /mnt/
    kpartx -d /dev/…
    exit
    $ gnt-instance deactivate-disks INSTANCE

