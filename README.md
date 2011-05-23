Ganeti Tutorial
===============

A tutorial on [Ganeti](http://code.google.com/p/ganeti/), a cluster
virtualization management tool created by Google. Its planned to be presented at
[Open Source Bridge 2011](http://opensourcebridge.org/) and [OSCON
2011](http://oscon.com).

This presentation was created with
[showoff](https://github.com/schacon/showoff). To see the presentation, run `gem
install showoff` then run `showoff serve` in this directory.

Outline
=======

Here's an outline of the tutorial as it stands now.

1. Introduction to Ganeti
    1. Basic overview
    2. Project history, background, and motivation
    3. Tutorial overview
2. Comparing to other projects
    1. Openstack
    2. Eucalyptus
    3. OpenNebula 
3. Base architecture
    1. Components
    2. Clusters, Nodes, & Instances
    3. Storage Management
    4. Network setup
4. Planning your cluster
    1. Hardware considerations
    2. Operating system
    3. Network
5. Installing Ganeti
    1. Installing the Hypervisor
    2. Installing optional software
    3. Setting up the network
    4. Configure LVM
    5. Install Ganeti
    6. Install OS Definition
    7. Initialize Ganeti
    8. Post-install steps
    9. Common setup issues
6. Virtual machines
    1. Overview
    2. Pros/Cons
    3. Deployment strategies
    4. VM Creation
    5. Common VM operations
7. Allocation tools
    1. Htools
    2. hail
    3. hspace
    4. hbal
8. Dealing with failures
    1. Node failures
    2. Disk failures
    3. Split brain
9. Other commands
    1. Cluster info
    2. Modifying cluster defaults
    3. Node info
    4. Modifying node information
    5. Exporting/Importing VMs
    6. Job queue
    7. Node Groups
10. Expanding a cluster
    1. Planning
    2. Adding node
    3. Rebalancing cluster
11. Upgrading Ganeti
    1. Common practices
    2. Procedure
    3. Potential issues
12. Extending with the RAPI
    1. Summary
    2. Common uses
14. Project Roadmap
    1. Release schedule
    2. Upcoming features 
13. Ganeti Web Manager
    1. Overview, project history, motivation
    2. Installation requirements
    3. Installation
    4. Using GWM
14. Conclusion

Credits
=======

* [Lance Albertson](http://lancealbertson.com)
* [Peter Krenesky](http://blogs.osuosl.org/kreneskyp/)

Copyright
=========

This work is licensed under a [Creative Commons Attribution-Share Alike 3.0
United States License](http://creativecommons.org/licenses/by-sa/3.0/us/).

vi: set tw=80 ft=markdown :
