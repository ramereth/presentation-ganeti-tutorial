!SLIDE commandline medcode bullets

# Export/Import

    $ gnt-backup export -n TARGET_NODE INSTANCE_NAME

* Create _snapshot_ of disk & configuration
* Backup, or import into another cluster
* _One_ snapshot for an instance

!SLIDE commandline bigcode

# Importing an instance

    $ gnt-backup import \
        -n TARGET_NODE \
        --src-node=NODE \
        --src-dir=DIR INSTANCE_NAME
