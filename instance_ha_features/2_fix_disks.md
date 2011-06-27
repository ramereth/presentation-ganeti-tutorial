!SLIDE bullets list rvc smtitle

# Restoring redundancy for DRBD-based instances

* _Primary_ node storage failed
    * Re-create disks on it
* _Secondary_ node storage failed
    * Re-create disks on secondary node
    * Change secondary

!SLIDE commandline incremental

# Replacing disks

    $ # re-create disks on the primary node
    gnt-instance replace-disks -p INSTANCE_NAME

    $ # re-create disks on the current secondary
    gnt-instance replace-disks -s INSTANCE_NAME

    $ # change the secondary node, via manual 
    $ # specification
    gnt-instance replace-disks -n NODE INSTANCE_NAME

    $ # change the secondary node, via an iallocator
    $ # script
    gnt-instance replace-disks -I SCRIPT INSTANCE_NAME

    $ # automatically fix the primary or secondary node
    gnt-instance replace-disks -a INSTANCE_NAME

