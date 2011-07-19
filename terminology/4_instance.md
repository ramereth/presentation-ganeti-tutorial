!SLIDE center bullets list smimg smtitle

# Instances

![instances](instances.png)

* Virtual machine that _runs_ on the cluster
* _fault tolerant/HA_ entity within cluster

!SLIDE bullets redcode list

# Instance Parameters

* Hypervisor (called `hvparams`)
* General (called `beparams`)
* Networking (called `nicparams`)
* _Modified_ via instance or cluster defaults

!SLIDE bullets list

# hvparams

* Boot order, CDROM Image
* NIC Type, Disk Type
* VNC Parameters, Serial console
* Kernel Path, initrd, args
* Other Hypervisor specific parameters

!SLIDE bullets list

# beparams
# nicparams

* Memory / Virtual CPUs
* MAC
* NIC mode (routed or bridged)
* Link

!SLIDE bullets list

# Disk template

* **drbd** : LVM + DRBD between 2 nodes
* **plain** : LVM w/ no redundancy
* **file** : Plain files, no redundancy
* **diskless** : Special purposes
