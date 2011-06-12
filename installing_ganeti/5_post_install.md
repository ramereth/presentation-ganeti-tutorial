!SLIDE 

# Post-install Steps

!SLIDE commandline bullets list redcode bigcode incremental

# Joining additional nodes

    $ gnt-node add \
        --secondary-ip 192.168.16.141 \
        node2.example.org

* ``--secondary-ip`` - DRBD node IP
* ``node2.example.org`` - node to add

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

* Does the hardware work?
* Can the Hypervisor create instances?
* Does each operation work properly? 
