!SLIDE commandline medcode bullets

# Export/Import

    $ gnt-backup export -n TARGET_NODE INSTANCE_NAME

* Create snapshot of disk & configuration
* Backup, or import into another cluster
* One snapshot for an instance

!SLIDE commandline bigcode

# Importing an instance

    $ gnt-backup import \
        -n TARGET_NODE \
        --src-node=NODE \
        --src-dir=DIR INSTANCE_NAME
