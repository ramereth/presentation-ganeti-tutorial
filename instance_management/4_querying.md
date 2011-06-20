!SLIDE bullets list

# Querying Instances

* **Two methods:**
    * listing instances
    * detailed instance information
* One useful for grep
* Other has more details, slower

!SLIDE commandline tiny

# Listing instances


    $ gnt-instance list
    Instance                  Hypervisor OS                          Primary_node      Status     Memory
    instance1.example.org     kvm        image+gentoo-hardened       node1.example.org ERROR_down      -
    instance2.example.org     kvm        image+centos                node2.example.org running      512M
    instance3.example.org     kvm        image+debian-squeeze        node1.example.org running      512M
    instance4.example.org     kvm        image+ubuntu-lucid          node2.example.org running      512M


!SLIDE commandline smcommandline tiny smtitle

# Detailed Instance Info

    $ gnt-instance info instance2
    Instance name: instance2.example.org
    UUID: 5b5b1c35-23de-45bf-b125-a9a001b2bebb
    Serial number: 22
    Creation time: 2011-05-24 23:05:44
    Modification time: 2011-06-15 21:39:12
    State: configured to be up, actual state is up
      Nodes:   
        - primary: node2.example.org
        - secondaries: 
      Operating system: image+centos
      Allocated network port: 11013
      Hypervisor: kvm
        - console connection: vnc to node2.example.org:11013 (display 5113)
        - acpi: True
        ...
      Hardware:
        - VCPUs: 2
        - memory: 512MiB
        - NICs:
          - nic/0: MAC: aa:00:00:39:4b:b5, IP: None, mode: bridged, link: br113
      Disk template: plain
      Disks:
        - disk/0: lvm, size 9.8G
          access mode: rw
          logical_id:  ganeti/0c3f6913-cc3d-4132-bbbf-af9766a7cde3.disk0
          on primary:  /dev/ganeti/0c3f6913-cc3d-4132-bbbf-af9766a7cde3.disk0 (252:3)
