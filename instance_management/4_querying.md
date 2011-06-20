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


!SLIDE commandline tiny smtitle

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
        - boot_order: disk
        - cdrom2_image_path: default ()
        - cdrom_disk_type: default ()
        - cdrom_image_path: 
        - disk_cache: default (default)
        - disk_type: paravirtual
        - floppy_image_path: default ()
        - initrd_path: 
        - kernel_args: ro
        - kernel_path: /boot/guest/vmlinuz-x86_64-hardened
        - kvm_flag: 

!SLIDE codeblock tiny greencode smtitle

# Detailed Instance Info

        - mem_path: 
        - migration_downtime: 30
        - nic_type: paravirtual
        - root_path: /dev/vda2
        - security_domain: 
        - security_model: pool
        - serial_console: True
        - usb_mouse: 
        - use_chroot: False
        - use_localtime: False
        - vhost_net: default (False)
        - vnc_bind_address: 0.0.0.0
        - vnc_password_file: default ()
        - vnc_tls: False
        - vnc_x509_path: 
        - vnc_x509_verify: False
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
