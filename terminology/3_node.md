!SLIDE bullets list

# Nodes

* _Physical_ machine
* Fault tolerance not _required_
* Added/removed _at will_ from cluster
* No _data loss_ with loss of node

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
