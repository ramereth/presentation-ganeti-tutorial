!SLIDE commandline medcode smbullets list

# Import of foreign instances

    $ gnt-instance add -t plain -n HOME_NODE ... \
        --disk 0:adopt=lv_name[,vg=vg_name] \
        INSTANCE_NAME

* Already stored as LVM volumes
* Ensure non-managed instance is stopped
* Take over given logical volumes
* Better transition
