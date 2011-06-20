!SLIDE bullets list redcode

# IAllocator

* Automatic placement of instances
* External scripts used to compute
* Eliminates manual node specification
* Found in ``lib/ganeti/iallocators``
* **htools**

!SLIDE smtitle bullets list

# _Primary_ & _Secondary_ concepts

* Always runs on _primary_
* Depends on _disk template_
* Uses secondary node for _disk replication_

!SLIDE bullets list

# Tags

* _Short strings_ attached to cluster, nodes, or instances
* Useful for attaching _owner information_
* Used by _external applications_ such as GWM

!SLIDE bullets list

# Jobs & OpCodes

* _OpCode_ = **Operation Code**
* Executed as part of a _Job_
* Single jobs executed _serially_
* _Parallellization_ when resources are available 
* Job _locking_

!SLIDE commandline bigcode smtitle bullets

# Jobs/OpCode example

    $ gnt-instance shutdown --all

*  
* Separate job containing _shutdown instance_ 
