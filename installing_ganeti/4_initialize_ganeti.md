!SLIDE subsec

# Initialize Ganeti

!SLIDE bullets list redcode rvc

# Cluster name

### **Mandatory** once per cluster, on the first node.

* Cluster hostname _resolvable_ by all nodes
* IP reserved **exclusively** for the cluster
* Used by _master_ node
* i.e.: ``ganeti-prod.example.org``

!SLIDE commandline rvc medcode

# Initialization

### KVM example

    $ gnt-cluster init \
        --master-netdev=br0 \
        --vg-name ganeti \
        --secondary-ip 192.168.16.16 \
        --enabled-hypervisors=kvm \
        --nic-parameters link=br0 \
        --backend-parameters \
            vcpus=1,memory=128M \
        --hypervisor-parameters \
            kvm:kernel_path=/boot/vmlinuz-2.6-kvmU \
            vnc_bind_address=0.0.0.0 \
        ganeti.example.org

!SLIDE codeblock rvc bigcode smtitle

# Cluster init args

### Master Network Device

    --master-netdev=br0

### Volume Group Name

    --vg-name ganeti

### DRBD Interface

    --secondary-ip 192.168.16.16

### Enabled Hypervisors

    --enabled-hypervisors=kvm

!SLIDE codeblock rvc bigcode smtitle

# Cluster init args

### Default NIC

    --nic-parameters link=br0

### Default Backend parameters

    --backend-parameters vcpus=1,memory=128M

### Default Hypervisor Parameters

    --hypervisor-parameters \
        kvm:kernel_path=/boot/vmlinuz-2.6-kvmU, \
        vnc_bind_address=0.0.0.0 \

### Cluster hostname

    ganeti.example.org

!SLIDE subsec

# Hands on
## Ganeti Initialization
