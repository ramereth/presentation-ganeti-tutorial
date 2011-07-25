!SLIDE bullets list smtitle

# Operating System Setup

* Clean, minimal system install
* Minimum _20GB_ system volume
* _Single_ LVM Volume Group for instances
* 64bit is preferred
* _Similar_ hardware/software configuration across nodes

!SLIDE medtable rvc

# Partition Setup

### typical layout

<table class="rdata">
    <tr class="odd">
        <td>/dev/sda1</td>
        <td>/boot</td>
        <td>200M</td>
    </tr>
    <tr class="even">
        <td>/dev/sda2</td>
        <td>/</td>
        <td>10-20G</td>
    </tr>
    <tr class="odd">
        <td>/dev/sda3</td>
        <td>LVM</td>
        <td>rest, named ganeti</td>
    </tr>
</table>

!SLIDE bullets list redcode

# Hostname Issues

* Requires _hostname_ to be the **FQDN**
* i.e. _node1.example.com_ instead of _node1_
* `hostname --fqdn` requires resolver library
* Reduce dependency on DNS and _guessing_
