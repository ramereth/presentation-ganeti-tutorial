!SLIDE bullets list

# Node Groups

* All nodes in same _pool_
* Nodes not equally _connected_ sometimes
* Cluster-wide _job locking_

!SLIDE bullets list redcode

# Node Group Attributes

* At least _one_ group
* `alloc_policy`: unallocable, last_resort, & preferred
* P/S nodes must be in the _same group_ for an instance
* Group _moves_ are possible

!SLIDE codeblock bigcode

# Node Group Management

    # add a new node group
    gnt-group add <group>

    # delete an empty node group
    gnt-group remove <group>
    
    # list node groups
    gnt-group list
    
    # rename a node group
    gnt-group rename <oldname> <newname>
    
!SLIDE codeblock bigcode

# Node Group Management

    # list only nodes belonging to a node group
    gnt-node {list,info} -g <group>

    $ gnt-group list
    Group   Nodes Instances AllocPolicy NDParams
    default     5        74 preferred   (empty)
    
    # assign a node to a node group
    gnt-node modify -g <group>
