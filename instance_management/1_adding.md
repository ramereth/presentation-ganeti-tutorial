!SLIDE bullets list rvc redcode

# Adding an instance

### Requires at least 5 params

* OS for the instance (`gnt-os list`)
* Disk template
* Disk count & size
* Node or iallocator
* Instance name (_resolvable_)

!SLIDE subsec

# Hands-on

## Deploying VMs

!SLIDE commandline bigcode

# Add Command

    $ gnt-instance add \
        -n TARGET_NODE:SECONDARY_NODE \
        -o OS_TYPE \
        -t DISK_TEMPLATE -s DISK_SIZE \
        INSTANCE_NAME

!SLIDE bullets list redcode rvc

# Other options

### among others

* Memory size (`-B memory=1GB`)
* Number of virtual CPUs (`-B vcpus=4`) 
* NIC settings (`--nic 0:link=br100`)
* `batch-create`
* See `gnt-instance` manpage for others
