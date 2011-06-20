!SLIDE bullets list

# Evacuating nodes

* Moving the _primary_ instances
* Moving _secondary_ instances

!SLIDE commandline bigcode

# Primary Instance conversion

    $ gnt-node migrate NODE
    $ gnt-node evacuate NODE

!SLIDE commandline medcode incremental

# Secondary instance evacuation

    $ # compute new secondary for each instance using 
    $ # iallocator
    gnt-node evacuate -I IALLOCATOR_SCRIPT NODE

    $ # simply move all instances to DESTINATION_NODE
    gnt-node evacuate -n DESTINATION_NODE NODE

!SLIDE commandline bigcode bullets

# Node Removal

    $ gnt-node remove NODE_NAME

* _Deconfigure_ node
* _Stop_ ganeti daemons
* Node in _clean_ state
