!SLIDE bullets list

# Nodes

* _Physical_ machine
* Fault tolerance not _required_
* Added/removed _at will_ from cluster
* No _data loss_ with loss of node

!SLIDE bullets list

# Node Roles

* **master**
    * Node which controls the cluster
* **master candidate**
    * Has full cluster config & knowledge
    * Can become a master node

!SLIDE bullets list

# Node Roles

* **regular**
    * most node state on bigger clusters
* **drained**
    * Working but cannot take new _instances_
    * Has hardware issues & may be evacuated soon

!SLIDE bullets list

# Node Roles

* **offline**
    * Daemons will not talk to this node
    * Instances flagged as an error in cluster verify

!SLIDE smbullets

# Node Daemons

* **`ganeti-noded`** : control hardware resources, runs on all
* **`ganeti-confd`** : only functional on master, runs on all
* **`ganeti-rapi`** : offers HTTP-based API for cluster, runs on master
* **`ganeti-masterd`** : allows control of cluster, runs on master

!SLIDE bullets list

# Node Flags

* **master_capable** : Remote node only runs local instances
* **vm_capable** : master candidate for configuration backups
