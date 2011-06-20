!SLIDE bullets list

# Upgrade notes

* Nodes daemons _restarted_ after upgrade
* _Backup_ config data
* _Live_ upgrades

!SLIDE commandline incremental medcode

# Upgrade Steps

    $ # Ensure no jobs are running (master only)
    gnt-job list
    
    $ # Stop all daemons on all nodes
    /etc/init.d/ganeti stop

    $ # Backup old config (master only)
    tar czf /var/lib/ganeti-$(date +%FT%T).tar.gz \
        -C /var/lib ganeti

    $ # Install new Ganeti version on all nodes
    $ # Run cfgupgrade on master node
    /usr/lib/ganeti/tools/cfgupgrade --verbose

    $ # Restart daemons on all nodes
    /etc/init.d/ganeti restart

!SLIDE commandline incremental medcode

# Upgrade Steps

    $ # Re-distribute configuration (master only)
    gnt-cluster redist-conf

    $ # Restart daemons again on all nodes
    /etc/init.d/ganeti restart

    $ # Verify cluster (master only)
    gnt-cluster verify
