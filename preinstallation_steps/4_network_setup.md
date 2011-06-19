!SLIDE subsec

# Network Setup

!SLIDE bullets

# Interface Layout

### network diagram

* **eth0** - trunked VLANs
* **eth1** - private DRBD network

!SLIDE codeblock bigcode rvc

# VLAN setup

### for Debian/Ubuntu

    allow-hotplug eth0
    allow-hotplug eth1
    allow-hotplug vlan100
    allow-hotplug vlan42

    auto vlan100
    iface vlan100 inet manual
        vlan_raw_device eth0

    auto vlan42
    iface vlan42 inet manual
        vlan_raw_device eth0

!SLIDE codeblock rvc

# Bridge setup

### for Debian/Ubuntu

    allow-hotplug br42
    allow-hotplug br10

    auto br42
    iface br42 inet static
       address 10.1.0.140
       netmask 255.255.254.0
       network 10.1.0.0
       broadcast 10.1.1.255
       gateway 10.1.0.1
       dns-nameservers 10.1.0.130
       dns-search example.org
       bridge_ports vlan42
       bridge_stp off
       bridge_fd 0

    auto br100
    iface br100 inet manual
       bridge_ports vlan100
       bridge_stp off
       bridge_fd 0

!SLIDE codeblock bigcode rvc

# DRBD Network setup

### for Debian/Ubuntu

    iface eth1 inet static
        address 192.168.16.140
        netmask 255.255.255.0
        network 192.168.16.0
        broadcast 192.168.16.255

!SLIDE bullets list

# Extending networking

* Ethernet bonding
* Redundancy
* Increase throughput 
