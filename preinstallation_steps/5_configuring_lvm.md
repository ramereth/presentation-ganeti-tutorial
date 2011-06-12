!SLIDE commandline bigcode

# Configuring LVM

    $ pvcreate /dev/sda3
    $ vgcreate ganeti /dev/sda3

!SLIDE codeblock bigcode rvc

# lvm.conf changes

### Ignore drbd devices

    filter = ["r|/dev/cdrom|", "r|/dev/drbd[0-9]+|" ]
