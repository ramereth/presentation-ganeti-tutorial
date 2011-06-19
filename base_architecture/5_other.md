!SLIDE bullets list redcode

# IAllocator

* Automatic placement of instances
* External scripts used to compute
* Eliminates manual node specification
* Found in ``lib/ganeti/iallocators``

!SLIDE bullets list

# _Primary_ & _Secondary_ concepts

* Depends on disk template
* Always runs on primary
* Uses secondary node for disk replication

!SLIDE bullets list

# Tags

* Short strings attached to cluster, nodes, or instances
* Useful for attaching owner information
* Listing instances by tags

!SLIDE bullets list

# Jobs & OpCodes

* _OpCode_ = Operation Code
* Executed as part of a _Job_
* Single jobs executed _serially_
* _Parallellization_ when resources are available 
* Job _lock_ priorities

!SLIDE commandline bigcode

# Jobs/OpCode example

### Separate job containing _shutdown instance_ 

    $ gnt-instance shutdown --all

