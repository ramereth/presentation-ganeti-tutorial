!SLIDE subsec

# Post-install Steps

!SLIDE commandline incremental bullets list rvc

# Testing/Viewing the nodes

    $ gnt-node list
    Node              DTotal DFree MTotal MNode MFree Pinst Sinst
    node1.example.org 223.4G 96.4G   7.8G  5.4G  2.7G     0     0
    node2.example.org 223.4G 96.4G   7.8G  5.4G  2.7G     0     0

* Ganeti damons can talk to each other
* Ganeti can examine storage on the nodes _(DTotal/DFree)_
* Ganeti can talk to the selected hypervisor _(MTotal/MNode/MFree)_

!SLIDE commandline bullets list incremental

# Cluster burnin testing

    $ /usr/lib/ganeti/tools/burnin -o image -p instance{1..5}

* Does the _hardware_ work?
* Can the _Hypervisor_ create instances?
* Does each _operation_ work properly? 
