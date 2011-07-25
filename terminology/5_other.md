!SLIDE bullets list redcode

# IAllocator

* Automatic placement of instances
* Eliminates manual node specification
* **htools**
* External scripts used to compute

!SLIDE bullets list recode

# Components

* Automatic allocation
* **hbal** : Cluster rebalancer
* **hail** : IAllocator script
* **hspace** : Cluster capacity estimator

!SLIDE smtitle bullets list himg center

# _Primary_ & _Secondary_ concepts

![primary-secondary](primary-secondary.png)

* Instances always runs on _primary_
* Uses secondary node for _disk replication_
* Depends on _disk template_ (i.e. drbd)
