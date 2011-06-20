!SLIDE bullets list

# Instances

* Virtual machine that _runs_ on the cluster
* _fault tolerant/HA_ entity within cluster

!SLIDE bullets redcode list

# Instance Parameters

* Hypervisor (called `hvparams`)
* General (called `beparams`)
* Per network-card (called `nicparams`)
* Modified via instance or cluster defaults

!SLIDE bullets list

# Disk template

* **diskless** : Special purposes
* **file** : Plain files, no redundancy
* **plain** : LVM w/ no redundancy
* **drbd** : LVM + DRBD between 2 nodes
