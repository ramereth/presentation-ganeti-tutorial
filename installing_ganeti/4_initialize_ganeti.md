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
        --master-netdev=br42 \
        --vg-name ganeti \
        --secondary-ip 192.168.16.140 \
        --enabled-hypervisors=kvm \
        --nic-parameters link=br100 \
        --backend-parameters \
            vcpus=2,memory=512M \
        --hypervisor-parameters \
            kvm:kernel_path=/boot/guest/vmlinuz \
            vnc_bind_address=0.0.0.0 \
        ganeti-prod.example.org

!SLIDE codeblock rvc bigcode smtitle

# Cluster init args

### Master Network Device

    --master-netdev=br42

### Volume Group Name

    --vg-name ganeti

### DRBD Interface

    --secondary-ip 192.168.16.140

### Enabled Hypervisors

    --enabled-hypervisors=kvm

!SLIDE codeblock rvc bigcode smtitle

# Cluster init args

### Default NIC

    --nic-parameters link=br100

### Default Backend parameters

    --backend-parameters vcpus=2,memory=512M

### Default Hypervisor Parameters

    --hypervisor-parameters \
        kvm:kernel_path=/boot/guest/vmlinuz-guest, \
        vnc_bind_address=0.0.0.0 \

### Cluster hostname

    ganeti-prod.example.org
