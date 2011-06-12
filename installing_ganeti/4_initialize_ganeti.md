!SLIDE subsec

# Initialize Ganeti

!SLIDE bullets list redcode rvc

# Cluster name

### **Mandatory** once per cluster, on the first node.

* Cluster hostname _resolvable_ by all nodes
* IP reserved **exclusively** for the cluster
* Used by _master_ node
* i.e.: ``ganeti-prod.example.org``

!SLIDE codeblock rvc bigcode

## Cluster init args

### Master Network Device

    --master-netdev=br42

### Volume Group Name

    --vg-name ganeti

### DRBD Interface

    --secondary-ip 192.168.16.140

### Enabled Hypervisors

    --enabled-hypervisors=kvm

!SLIDE codeblock rvc bigcode

## Cluster init args

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

!SLIDE commandline incremental

# Testing the Cluster

    $ gnt-cluster verify
    Sun Jun 12 20:32:37 2011 * Verifying global settings
    Sun Jun 12 20:32:37 2011 * Gathering data (1 nodes)
    Sun Jun 12 20:32:45 2011 * Gathering disk information (1 nodes)
    Sun Jun 12 20:33:15 2011 * Verifying node status
    Sun Jun 12 20:33:15 2011 * Verifying instance status
    Sun Jun 12 20:33:15 2011 * Verifying orphan volumes
    Sun Jun 12 20:33:15 2011 * Verifying orphan instances
    Sun Jun 12 20:33:15 2011 * Verifying N+1 Memory redundancy
    Sun Jun 12 20:33:15 2011 * Other Notes
    Sun Jun 12 20:33:15 2011 * Hooks Results

