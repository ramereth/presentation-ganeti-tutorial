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

!SLIDE redcode medtable

# Node Daemons

<table class="rdata">
    <tr class="odd">
        <td><code><b>ganeti-noded</b></code></td>
        <td>control hardware resources, runs on all</td>
    </tr>
    <tr class="even">
        <td><code><b>ganeti-confd<b></code></td>
        <td>only functional on master, runs on all</td>
    </tr>
    <tr class="odd">
        <td><code><b>ganeti-rapi<b></code></td>
        <td>offers HTTP-based API for cluster, runs on master</td>
    </tr>
    <tr class="even">
        <td><code><b>ganeti-masterd</b></code></td>
        <td>allows control of cluster, runs on master</td>
    </tr>
</table>

!SLIDE redcode medtable

# Node Flags

<table class="rdata">
    <tr class="odd">
        <td><code><b>master_capable</b></code></td>
        <td>Remote node only runs local instances</td>
    </tr>
    <tr class="even">
        <td><code><b>vm_capable<b></code></td>
        <td>master candidate for configuration backups</td>
    </tr>
</table>
