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
    1. Project history, background, and motivation
    1. Tutorial overview
1. Hands-on Setup
    1. VM images
    1. How the Hands-on VMs are setup
1. Comparing to other projects
    1. Openstack
    1. Eucalyptus
    1. OpenNebula 
1. Base architecture
    1. Components
    1. Clusters, Nodes, & Instances
    1. Storage Management
    1. Network setup
1. Planning your cluster
    1. Hardware Planning
    1. Operating system
    1. Network
1. Pre-installation Steps
    1. Operating System Setup
    1. Installing the Hypervisor
    1. Installing DRBD 
    1. Network Setup
    1. Configuring LVM
1. Installing Ganeti
    1. Install Ganeti
    1. Install OS Definition
    1. Initialize Ganeti
    1. Post-install steps
1. Virtual machines
    1. Overview
    1. Pros/Cons
    1. Deployment strategies
    1. VM Creation
    1. Common VM operations
1. Allocation tools
    1. Htools
    1. hail
    1. hspace
    1. hbal
1. Dealing with failures
    1. Node failures
    1. Disk failures
    1. Split brain
1. Other commands
    1. Cluster info
    1. Modifying cluster defaults
    1. Node info
    1. Modifying node information
    1. Exporting/Importing VMs
    1. Job queue
    1. Node Groups
1. Expanding a cluster
    1. Planning
    1. Adding node
    1. Rebalancing cluster
1. Upgrading Ganeti
    1. Common practices
    1. Procedure
    1. Potential issues
1. Extending with the RAPI
    1. Summary
    1. Common uses
1. Project Roadmap
    1. Release schedule
    1. Upcoming features 
1. Ganeti Web Manager
    1. Overview, project history, motivation
    1. Installation requirements
    1. Installation
    1. Using GWM
1. Conclusion

Credits
=======

* [Lance Albertson](http://lancealbertson.com)
* [Peter Krenesky](http://blogs.osuosl.org/kreneskyp/)

Copyright
=========

This work is licensed under a [Creative Commons Attribution-Share Alike 3.0
United States License](http://creativecommons.org/licenses/by-sa/3.0/us/).

vi: set tw=80 ft=markdown :
