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

1. Introduction to Ganeti (3min)
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
1. Terminology (12min)
    1. Components
    1. Terminology
    1. Nodes
    1. Instances
    1. Other
1. Planning your cluster (5min)
    1. Hardware Planning
    1. Operating system
    1. Network
1. Pre-installation Steps (11min)
    1. Operating System Setup
    1. Installing the Hypervisor
    1. Installing DRBD 
    1. Network Setup
    1. Configuring LVM
1. Installing Ganeti (15min)
    1. Install Ganeti
    1. Install Instance Image
    1. Initialize Ganeti
    1. Post-install steps
1. Instance Management (8min)
    1. Adding
    1. Removal
    1. Startup/Shutdown
    1. Querying
    1. Import/Export
    1. Import Foreign
    1. Kernel settings
1. Instance HA Features
    1. Change Primary
    1. Fix Disks
    1. Convert Disk Type
1. Instance Debugging
    1. Accessing Instance Disks
    1. Console access
1. Node Operations
    1. Adding a node
    1. Master Failover
    1. Evacuate
1. Job Operations
    1. Querying
1. Htools
    1. hail
    1. hspace
    1. hbal
1. Upgrading Ganeti
    1. Common practices
    1. Procedure
    1. Potential issues
1. RAPI
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
