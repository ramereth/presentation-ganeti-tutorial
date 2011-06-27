!SLIDE bullets list

# Evacuating nodes

* Moving the _primary_ instances
* Moving _secondary_ instances

!SLIDE commandline bigcode

# Primary Instance conversion

    $ gnt-node migrate NODE
    $ gnt-node evacuate NODE

!SLIDE commandline bigcode bullets

# Node Removal

    $ gnt-node remove NODE_NAME

* _Deconfigure_ node
* _Stop_ ganeti daemons
* Node in _clean_ state
