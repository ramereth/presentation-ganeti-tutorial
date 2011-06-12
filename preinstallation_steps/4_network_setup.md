!SLIDE

# Network Setup

!SLIDE bullets

# Interface layout

## <network diagram>

* _eth0_ - trunked VLANs
* _eth1_ - private DRBD network

!SLIDE codeblock

# VLAN setup

### for Debian/Ubuntu

<pre>
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
</pre>

!SLIDE codeblock

# Bridge setup

### for Debian/Ubuntu

<pre>
allow-hotplug br42
allow-hotplug br100

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
</pre>

!SLIDE codeblock

# DRBD Network setup

### for Debian/Ubuntu

<pre>
iface eth1 inet static
    address 192.168.16.140
    netmask 255.255.255.0
    network 192.168.16.0
    broadcast 192.168.16.255
</pre>

!SLIDE bullets list

# Extending networking

* Ethernet bonding
* Redundancy
* Increase throughput 
